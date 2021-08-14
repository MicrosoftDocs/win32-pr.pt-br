---
title: O que é uma interface COM
description: O que é uma interface COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a6eac63fb6395e04f36c89826a392046c906a70105e19bb6b9514975d89197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387591"
---
# <a name="what-is-a-com-interface"></a>O que é uma interface COM?

Se você conhece C# ou Java, as interfaces devem ser um conceito familiar. Uma *interface* define um conjunto de métodos aos quais um objeto pode dar suporte, sem ditar nada sobre a implementação. A interface marca um limite claro entre o código que chama um método e o código que implementa o método. Em termos de ciência da computação, o chamador é *dissociado* da implementação.

![ilustração mostrando o limite de interface entre um objeto e um aplicativo](images/com01.png)

Em C++, o equivalente mais próximo a uma interface é uma classe virtual pura, ou seja, uma classe que contém apenas métodos virtuais puros e nenhum outro membro. Aqui está um exemplo hipotético de uma interface:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

A ideia desse exemplo é que um conjunto de objetos em alguma biblioteca de gráficos é desenhável. A `IDrawable` interface define as operações que qualquer objeto que pode ser desenhado deve dar suporte. (Por convenção, os nomes de interface começam com "I".) Neste exemplo, a `IDrawable` interface define uma única operação: `Draw` .

Todas as interfaces são *abstratas*, de modo que um programa não pôde criar uma instância de um `IDrawable` objeto como tal. Por exemplo, o código a seguir não seria compilado.

```C++
IDrawable draw;
draw.Draw();
```

Em vez disso, a biblioteca de gráficos fornece objetos que *implementam* a `IDrawable` interface. Por exemplo, a biblioteca pode fornecer um objeto de forma para desenhar formas e um objeto de bitmap para imagens de desenho. Em C++, isso é feito herdando-se de uma classe base abstrata comum:

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

As `Shape` `Bitmap` classes e definem dois tipos distintos de objeto desenhável. Cada classe herda de `IDrawable` e fornece sua própria implementação do `Draw` método. Naturalmente, as duas implementações podem diferir consideravelmente. Por exemplo, o `Shape::Draw` método pode rasterizar um conjunto de linhas, enquanto `Bitmap::Draw` blit uma matriz de pixels.

Um programa que usa essa biblioteca de gráficos pode manipular `Shape` e `Bitmap` objetos por meio `IDrawable` de ponteiros, em vez de usar `Shape` ou `Bitmap` ponteiros diretamente.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Aqui está um exemplo que faz um loop em uma matriz de `IDrawable` ponteiros. A matriz pode conter uma variedade heterogênea de formas, bitmaps e outros objetos gráficos, desde que cada objeto na matriz seja herdado `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Um ponto importante sobre o COM é que o código de chamada nunca vê o tipo da classe derivada. Em outras palavras, você nunca declararia uma variável do tipo `Shape` ou `Bitmap` em seu código. Todas as operações em formas e bitmaps são executadas usando `IDrawable` ponteiros. Dessa forma, o COM mantém uma separação estrita entre a interface e a implementação. Os detalhes de implementação das `Shape` `Bitmap` classes e podem mudar, por exemplo, para corrigir bugs ou adicionar novos recursos, sem nenhuma alteração no código de chamada.

Em uma implementação do C++, as interfaces são declaradas usando uma classe ou estrutura.

> [!Note]  
> Os exemplos de código neste tópico destinam-se a transmitir conceitos gerais, não a prática do mundo real. Definir novas interfaces COM está além do escopo desta série, mas você não definiria uma interface diretamente em um arquivo de cabeçalho. Em vez disso, uma interface COM é definida usando um idioma chamado IDL (Interface Definition Language). O arquivo IDL é processado por um compilador IDL, que gera um arquivo de cabeçalho C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Quando você trabalha com com, é importante lembrar que as interfaces não são objetos. São coleções de métodos que os objetos devem implementar. Vários objetos podem implementar a mesma interface, conforme mostrado com os `Shape` `Bitmap` exemplos e. Além disso, um objeto pode implementar várias interfaces. Por exemplo, a biblioteca de gráficos pode definir uma interface chamada `ISerializable` que dá suporte ao salvamento e ao carregamento de objetos gráficos. Agora, considere as seguintes declarações de classe:

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

Neste exemplo, a `Bitmap` classe implementa `ISerializable` . O programa pode usar esse método para salvar ou carregar o bitmap. No entanto, a `Shape` classe não implementa `ISerializable` , portanto, não expõe essa funcionalidade. O diagrama a seguir mostra as relações de herança neste exemplo.

![ilustração mostrando a herança de interface, com as classes Shape e bitmap apontando para idrawable, mas somente bitmap apontando para ISerializable](images/com02.png)

Esta seção examinou a base conceitual das interfaces, mas até agora, não vimos o código COM real. Começaremos com a primeira coisa que qualquer aplicativo COM deve fazer: inicializar a biblioteca COM.

## <a name="next"></a>Avançar

[Inicializando a biblioteca COM](initializing-the-com-library.md)