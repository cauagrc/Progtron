<div align="center">

# Progtron

**Software educacional para apoio ao ensino de programação**

![JDK 21](https://img.shields.io/badge/JDK-21.0.10-red?style=flat-square&logo=openjdk&logoColor=white)
![JavaFX](https://img.shields.io/badge/JavaFX-21-blue?style=flat-square&logo=openjdk&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![OpenGL](https://img.shields.io/badge/OpenGL-5586A4?style=flat-square&logo=opengl&logoColor=white)
![GLFW](https://img.shields.io/badge/GLFW-000000?style=flat-square&logo=opengl&logoColor=white)
![GLM](https://img.shields.io/badge/GLM-Math-4B8BBE?style=flat-square)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)

</div>

> [!NOTE]
> O **"Progtron"** foi desenvolvido como parte do projeto **“Desenvolvimento de Softwares Educacionais por meio da Integração entre Programação Orientada a Objetos e Computação Gráfica”**, do curso de Ciência da Computação da Fundação Universidade Federal de Rondônia (UNIR).

O projeto busca integrar conhecimentos de **Programação Orientada a Objetos** e **Computação Gráfica** no desenvolvimento de uma aplicação educacional para computador.

---

## Sumário

- [Sobre](#sobre)
- [Configuração e instalação](#configuração-e-instalação)
- [Resumo](#resumo)
- [Autores](#autores)

---

## Sobre

> [!NOTE]
> Para visualizar o funcionamento da aplicação, consulte o [vídeo de demonstração](https://youtu.be/IQQOm2Efdlk).

O **Progtron** é um aplicativo educacional para computador desenvolvido com o objetivo de unir conceitos de **Programação Orientada a Objetos** e **Computação Gráfica** em uma aplicação interativa voltada ao ensino de programação.

O projeto foi desenvolvido de forma colaborativa por estudantes das disciplinas de Programação Orientada a Objetos e Computação Gráfica do curso de Ciência da Computação da **Universidade Federal de Rondônia (UNIR)**.

A aplicação busca proporcionar uma experiência prática de aprendizagem, utilizando elementos gráficos e interativos para apresentar conteúdos de programação e permitir que o usuário aplique seus conhecimentos durante a utilização do software.

## Configuração e instalação

> [!IMPORTANT]
> Caso prefira acompanhar visualmente o processo de instalação e configuração do projeto, utilize o [vídeo](https://youtu.be/AlDXS4Qw-UY).

Antes de executar o Progtron, é necessário instalar algumas dependências e compilar a biblioteca gráfica utilizada pela aplicação

### 1. Clonar os repositórios

O projeto utiliza dois repositórios:

- `progton-lib`: biblioteca gráfica utilizada pela aplicação;
- `progtron`: aplicação principal do Progtron.

Clone ambos utilizando:

```bash
git clone https://github.com/Tatmiki/progton-lib
git clone https://github.com/cauagrc/progtron
```

Após a clonagem, os dois diretórios devem estar localizados na mesma pasta:

```text
/
├── progton-lib/
└── progtron/
```

### 2. Pré-requisitos

Certifique-se de possuir as seguintes ferramentas instaladas:

- **JDK 21.0.10**
- **Maven**
- **GLM**

#### Dependências do sistema — Ubuntu/Debian

Instale as dependências abaixo:

```bash
sudo apt install libglfw3
sudo apt install libglfw3-dev
sudo apt install cmake
sudo apt install default-jdk
```

### 3. Instalação do GLM

Extraia o arquivo do **GLM** e acesse a pasta criada.

Em seguida, execute os comandos abaixo, um de cada vez:

```bash
cmake \
    -DGLM_BUILD_TESTS=OFF \
    -DBUILD_SHARED_LIBS=OFF \
    -B build .
```
```bash
cmake --build build --all
```
```bash
sudo cmake --build build --install
```

### 4. Compilando a biblioteca gráfica

Entre no repositório da biblioteca:

```bash
cd progton-lib
```

Altere para a branch correta:

```bash
git checkout feat/domain
```

Crie a pasta de build:

```bash
mkdir build
```

Configure o projeto:

```bash
cmake -B build -S .
```

Compile a biblioteca:

```bash
cmake --build build
```

Após a conclusão desse processo, a biblioteca estará pronta para ser utilizada pelo PROGTRON.

### 5. Executando o projeto

Retorne para o diretório da aplicação principal:

```bash
cd ../progtron
```

Execute utilizando Maven:

```bash
mvn javafx:run
```

Após a compilação das dependências, a aplicação deverá ser iniciada.

## Resumo

O processo completo consiste em:

1. Clonar `progton-lib`;
2. Clonar `progtron`;
3. Instalar JDK, Maven, CMake, GLFW e GLM;
4. Configurar e instalar o GLM;
5. Compilar a biblioteca `progton-lib`;
6. Executar a aplicação utilizando:

```bash
mvn javafx:run
```

## Autores

- **Cauã Galdino Garcia**, Universidade Federal de Rondônia (UNIR)
- **Marcus Vinícius Nascimento Pinheiro**, Universidade Federal de Rondônia (UNIR)
- **Samuel Gomes Cunha Amádio**, Universidade Federal de Rondônia (UNIR)
- **João Henrique Vieira do Carmo**, Universidade Federal de Rondônia (UNIR)
- **Leonardo Seiji Nakayama Prado**, Universidade Federal de Rondônia (UNIR)
- **Thiago Antônico Costa do Nascimento**, Universidade Federal de Rondônia (UNIR)
