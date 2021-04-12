---
title: O que é uma interface COM
description: O que é uma interface COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2019
ms.locfileid: "104364521"
---
# <a name="what-is-a-com-interface"></a><span data-ttu-id="97524-103">O que é uma interface COM?</span><span class="sxs-lookup"><span data-stu-id="97524-103">What Is a COM Interface?</span></span>

<span data-ttu-id="97524-104">Se você conhece C# ou Java, as interfaces devem ser um conceito familiar.</span><span class="sxs-lookup"><span data-stu-id="97524-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="97524-105">Uma *interface* define um conjunto de métodos aos quais um objeto pode dar suporte, sem ditar nada sobre a implementação.</span><span class="sxs-lookup"><span data-stu-id="97524-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="97524-106">A interface marca um limite claro entre o código que chama um método e o código que implementa o método.</span><span class="sxs-lookup"><span data-stu-id="97524-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="97524-107">Em termos de ciência da computação, o chamador é *dissociado* da implementação.</span><span class="sxs-lookup"><span data-stu-id="97524-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![ilustração mostrando o limite de interface entre um objeto e um aplicativo](images/com01.png)

<span data-ttu-id="97524-109">Em C++, o equivalente mais próximo a uma interface é uma classe virtual pura, ou seja, uma classe que contém apenas métodos virtuais puros e nenhum outro membro.</span><span class="sxs-lookup"><span data-stu-id="97524-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="97524-110">Aqui está um exemplo hipotético de uma interface:</span><span class="sxs-lookup"><span data-stu-id="97524-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="97524-111">A ideia desse exemplo é que um conjunto de objetos em alguma biblioteca de gráficos é desenhável.</span><span class="sxs-lookup"><span data-stu-id="97524-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="97524-112">A `IDrawable` interface define as operações que qualquer objeto que pode ser desenhado deve dar suporte.</span><span class="sxs-lookup"><span data-stu-id="97524-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="97524-113">(Por convenção, os nomes de interface começam com "I".) Neste exemplo, a `IDrawable` interface define uma única operação: `Draw` .</span><span class="sxs-lookup"><span data-stu-id="97524-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="97524-114">Todas as interfaces são *abstratas*, de modo que um programa não pôde criar uma instância de um `IDrawable` objeto como tal.</span><span class="sxs-lookup"><span data-stu-id="97524-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="97524-115">Por exemplo, o código a seguir não seria compilado.</span><span class="sxs-lookup"><span data-stu-id="97524-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="97524-116">Em vez disso, a biblioteca de gráficos fornece objetos que *implementam* a `IDrawable` interface.</span><span class="sxs-lookup"><span data-stu-id="97524-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="97524-117">Por exemplo, a biblioteca pode fornecer um objeto de forma para desenhar formas e um objeto de bitmap para imagens de desenho.</span><span class="sxs-lookup"><span data-stu-id="97524-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="97524-118">Em C++, isso é feito herdando-se de uma classe base abstrata comum:</span><span class="sxs-lookup"><span data-stu-id="97524-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

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

<span data-ttu-id="97524-119">As `Shape` `Bitmap` classes e definem dois tipos distintos de objeto desenhável.</span><span class="sxs-lookup"><span data-stu-id="97524-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="97524-120">Cada classe herda de `IDrawable` e fornece sua própria implementação do `Draw` método.</span><span class="sxs-lookup"><span data-stu-id="97524-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="97524-121">Naturalmente, as duas implementações podem diferir consideravelmente.</span><span class="sxs-lookup"><span data-stu-id="97524-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="97524-122">Por exemplo, o `Shape::Draw` método pode rasterizar um conjunto de linhas, enquanto `Bitmap::Draw` blit uma matriz de pixels.</span><span class="sxs-lookup"><span data-stu-id="97524-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="97524-123">Um programa que usa essa biblioteca de gráficos pode manipular `Shape` e `Bitmap` objetos por meio `IDrawable` de ponteiros, em vez de usar `Shape` ou `Bitmap` ponteiros diretamente.</span><span class="sxs-lookup"><span data-stu-id="97524-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="97524-124">Aqui está um exemplo que faz um loop em uma matriz de `IDrawable` ponteiros.</span><span class="sxs-lookup"><span data-stu-id="97524-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="97524-125">A matriz pode conter uma variedade heterogênea de formas, bitmaps e outros objetos gráficos, desde que cada objeto na matriz seja herdado `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="97524-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="97524-126">Um ponto importante sobre o COM é que o código de chamada nunca vê o tipo da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="97524-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="97524-127">Em outras palavras, você nunca declararia uma variável do tipo `Shape` ou `Bitmap` em seu código.</span><span class="sxs-lookup"><span data-stu-id="97524-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="97524-128">Todas as operações em formas e bitmaps são executadas usando `IDrawable` ponteiros.</span><span class="sxs-lookup"><span data-stu-id="97524-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="97524-129">Dessa forma, o COM mantém uma separação estrita entre a interface e a implementação.</span><span class="sxs-lookup"><span data-stu-id="97524-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="97524-130">Os detalhes de implementação das `Shape` `Bitmap` classes e podem mudar, por exemplo, para corrigir bugs ou adicionar novos recursos, sem nenhuma alteração no código de chamada.</span><span class="sxs-lookup"><span data-stu-id="97524-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="97524-131">Em uma implementação do C++, as interfaces são declaradas usando uma classe ou estrutura.</span><span class="sxs-lookup"><span data-stu-id="97524-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="97524-132">Os exemplos de código neste tópico destinam-se a transmitir conceitos gerais, não a prática do mundo real.</span><span class="sxs-lookup"><span data-stu-id="97524-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="97524-133">Definir novas interfaces COM está além do escopo desta série, mas você não definiria uma interface diretamente em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="97524-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="97524-134">Em vez disso, uma interface COM é definida usando um idioma chamado IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="97524-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="97524-135">O arquivo IDL é processado por um compilador IDL, que gera um arquivo de cabeçalho C++.</span><span class="sxs-lookup"><span data-stu-id="97524-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="97524-136">Quando você trabalha com com, é importante lembrar que as interfaces não são objetos.</span><span class="sxs-lookup"><span data-stu-id="97524-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="97524-137">São coleções de métodos que os objetos devem implementar.</span><span class="sxs-lookup"><span data-stu-id="97524-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="97524-138">Vários objetos podem implementar a mesma interface, conforme mostrado com os `Shape` `Bitmap` exemplos e.</span><span class="sxs-lookup"><span data-stu-id="97524-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="97524-139">Além disso, um objeto pode implementar várias interfaces.</span><span class="sxs-lookup"><span data-stu-id="97524-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="97524-140">Por exemplo, a biblioteca de gráficos pode definir uma interface chamada `ISerializable` que dá suporte ao salvamento e ao carregamento de objetos gráficos.</span><span class="sxs-lookup"><span data-stu-id="97524-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="97524-141">Agora, considere as seguintes declarações de classe:</span><span class="sxs-lookup"><span data-stu-id="97524-141">Now consider the following class declarations:</span></span>

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

<span data-ttu-id="97524-142">Neste exemplo, a `Bitmap` classe implementa `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="97524-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="97524-143">O programa pode usar esse método para salvar ou carregar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="97524-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="97524-144">No entanto, a `Shape` classe não implementa `ISerializable` , portanto, não expõe essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="97524-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="97524-145">O diagrama a seguir mostra as relações de herança neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="97524-145">The following diagram shows the inheritance relations in this example.</span></span>

![ilustração mostrando a herança de interface, com as classes Shape e bitmap apontando para idrawable, mas somente bitmap apontando para ISerializable](images/com02.png)

<span data-ttu-id="97524-147">Esta seção examinou a base conceitual das interfaces, mas até agora, não vimos o código COM real.</span><span class="sxs-lookup"><span data-stu-id="97524-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="97524-148">Começaremos com a primeira coisa que qualquer aplicativo COM deve fazer: inicializar a biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="97524-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="97524-149">Avançar</span><span class="sxs-lookup"><span data-stu-id="97524-149">Next</span></span>

[<span data-ttu-id="97524-150">Inicializando a biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="97524-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)