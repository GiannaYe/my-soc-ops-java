# Soc Ops  Workspace Instructions

## Development Checklist

**Before committing, run**:
`ash
cd socops
./mvnw clean package   # Build & compile
./mvnw test            # Run all tests
`

---

## Code Style

**Java 21 with Spring Boot 3.x**:
- Follow [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
- camelCase for methods/variables, PascalCase for classes
- Lines under 120 characters
- Constructor injection preferred over field injection

## Architecture

**Package Structure**:
- web/  REST controllers (@RestController)
- service/  Business logic (BoardAssembler)
- model/  POJOs (BingoCell, PlayPhase, WinningStreak)
- data/  Static data (IcebreakerPrompts)

**Game Logic**:
- 5x5 bingo board with icebreaker prompts
- Win: 5 marked cells in row (horizontal, vertical, diagonal)
- PlayPhase enum: SETUP, PLAYING, WON, LOST

## Build and Test

**Essential Commands**:
`ash
./mvnw clean package      # Build
./mvnw spring-boot:run    # Dev server (http://localhost:8080)
./mvnw test               # Run tests
`

**Requirements**: Java 21 JDK, Maven 3.8+

**Testing**: JUnit 5, naming: {ClassName}Tests.java

## Conventions

**REST**: GET /api/game, POST /api/game/move
**Naming**: Services end with Service or domain name (BoardAssembler)
**Models**: POJOs without Model suffix (BingoCell not BingoCellModel)
**Config**: All settings in application.properties (no hardcoded values)
**Frontend**: Thymeleaf templates, utility-first CSS, minimal JavaScript

## Common Tasks

**Add API endpoint**:
1. Define in BingoRestController
2. Implement in BoardAssembler
3. Add tests in src/test/
4. Test via ./mvnw spring-boot:run

**Modify prompts**: Edit IcebreakerPrompts.java and rebuild

**Debug**: Run ./mvnw spring-boot:run and check terminal logs

## References

- [Spring Boot Docs](https://spring.io/projects/spring-boot)
- [Thymeleaf](https://www.thymeleaf.org/)
- [CSS Utilities](.github/instructions/css-utilities.instructions.md)
