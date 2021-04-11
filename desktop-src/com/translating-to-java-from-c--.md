---
title: Convertendo para Java do C++
description: Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica. Os ponteiros de memória fornecem esse acesso direto. No Java, os ponteiros são tratados para você.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363713"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="a4e03-105">Convertendo para Java do C++</span><span class="sxs-lookup"><span data-stu-id="a4e03-105">Translating to Java from C++</span></span>

<span data-ttu-id="a4e03-106">Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica.</span><span class="sxs-lookup"><span data-stu-id="a4e03-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="a4e03-107">Os ponteiros de memória fornecem esse acesso direto.</span><span class="sxs-lookup"><span data-stu-id="a4e03-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="a4e03-108">No Java, os ponteiros são tratados para você.</span><span class="sxs-lookup"><span data-stu-id="a4e03-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="a4e03-109">Nos tipos de dados de composição Java, **struct**, **Union** e **typedef** são tratados exclusivamente pelo uso de classes.</span><span class="sxs-lookup"><span data-stu-id="a4e03-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="a4e03-110">Por exemplo, o tipo de dados **variante** do C++ é mapeado para **com. ms. com. Variant** em Java.</span><span class="sxs-lookup"><span data-stu-id="a4e03-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="a4e03-111">Em C++, Strings são uma matriz de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a4e03-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="a4e03-112">No Java, cadeias de caracteres são objetos.</span><span class="sxs-lookup"><span data-stu-id="a4e03-112">In Java, strings are objects.</span></span> <span data-ttu-id="a4e03-113">Os métodos que atuam em cadeias de caracteres tratam a cadeia como um objeto completo.</span><span class="sxs-lookup"><span data-stu-id="a4e03-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="a4e03-114">Os métodos COM retornam um valor conhecido como **HRESULT**, que é um código de erro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a4e03-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="a4e03-115">O suporte Java para o Microsoft Internet Explorer define uma classe, **com. ms. com. COMException**, que encapsula o código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4e03-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="a4e03-116">O Java não oferece suporte a tipos de dados não assinados, exceto **Char**, que é um inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a4e03-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="a4e03-117">Os métodos que aceitam ou retornam outros tipos de dados não assinados não podem ser usados no Java.</span><span class="sxs-lookup"><span data-stu-id="a4e03-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="a4e03-118">O Java não oferece suporte a matrizes multidimensionais.</span><span class="sxs-lookup"><span data-stu-id="a4e03-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="a4e03-119">Métodos que aceitam ou retornam matrizes multidimensionais não estão disponíveis no Java.</span><span class="sxs-lookup"><span data-stu-id="a4e03-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="a4e03-120">Valores Boolianos em Java não podem ser convertidos em 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="a4e03-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4e03-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4e03-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e03-122">Convertendo para Java</span><span class="sxs-lookup"><span data-stu-id="a4e03-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




