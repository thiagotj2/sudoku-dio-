# 🧩 Sudoku DIO — Projeto de Portfólio

> Projeto baseado no repositório oficial da DIO (`digitalinnovationone/sudoku`).  
> Objetivo: ter um projeto Java organizado no GitHub + uma pequena melhoria/documentação para o portfólio.

## 📌 Sobre
Implementação de Sudoku em **Java** (terminal e UI), usada como desafio do curso da **DIO**.  
Este repositório replica a base oficial e adiciona:
- Documentação clara de execução (terminal e UI).
- Arquivo com **argumentos de exemplo** para carregar um tabuleiro inicial.
- (Opcional) **CI** simples com GitHub Actions para compilar o projeto automaticamente.

## 🚀 Tecnologias
- Java 11+ (recomendado 17)
- Git & GitHub
- (Opcional) IntelliJ IDEA

## 📂 Estrutura sugerida
```
.
├── src/                  # código original
├── diagrams/             # opcional: seus diagramas (Draw.io)
├── design/               # opcional: protótipos/prints da UI
├── .github/workflows/    # CI (opcional)
├── puzzle_args.txt       # argumentos para rodar com puzzle de exemplo
└── README.md
```

## ▶️ Como executar (terminal)
> Ajuste o nome da classe principal se necessário (na base da DIO costuma ser algo como `br.com.dio.Main`).

### Usando IntelliJ (mais fácil)
1. `File > Open...` e selecione a pasta do projeto.
2. Abra a classe que contém `public static void main(String[] args)`.
3. Clique em **Run**.  
4. Para passar argumentos: `Run > Edit Configurations... > Program arguments` e cole o conteúdo de `puzzle_args.txt`.

### Via linha de comando (Unix/macOS/Linux)
```bash
mkdir -p out
# compila todas as .java dentro de src
find src -name "*.java" > sources.txt
javac -d out @sources.txt
# rode a classe principal (ajuste o nome se necessário)
java -cp out br.com.dio.Main "$(cat puzzle_args.txt)"
```

### Via linha de comando (Windows PowerShell)
```powershell
mkdir out
Get-ChildItem -Recurse -Filter *.java -Path src | ForEach-Object FullName > sources.txt
javac -d out @sources.txt
# rode a classe principal (ajuste o nome se necessário)
java -cp out br.com.dio.Main "$(Get-Content .\puzzle_args.txt)"
```

## 💡 Pequenas melhorias sugeridas (fáceis e que contam pontos)
- **README completo** (este aqui ✅).
- **CI** com GitHub Actions para compilar o projeto em cada push (arquivo incluso em `.github/workflows/java-ci.yml`).
- **Diagrama simples** no `diagrams/` (pode ser um retângulo com `Main -> Board -> Cell` feito no Draw.io).

## 🧪 Argumentos de exemplo
Use o arquivo `puzzle_args.txt` (incluído neste repositório). Ele contém exatamente a sequência usada no curso.

## 📚 Aprendizados
- POO em Java aplicada a um jogo
- Organização de projeto + versionamento com Git
- Documentação clara para rodar localmente

## 🔗 Links
- Repositório base (terminal): https://github.com/digitalinnovationone/sudoku
- Repositório base (UI): https://github.com/digitalinnovationone/sudoku/tree/ui
- Draw.io: https://app.diagrams.net
- Figma: https://www.figma.com/

---

> Dica: se você clonou o repositório oficial, crie um **repositório novo no seu GitHub** e troque o `origin` para apontar para ele. Se preferir, faça um **fork** e edite o README direto no navegador.
