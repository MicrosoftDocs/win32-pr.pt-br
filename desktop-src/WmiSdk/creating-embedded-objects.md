---
description: 'Ao criar uma instância com objetos inseridos, execute as seguintes tarefas:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Criando objetos inseridos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762434"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="b4412-103">Criando objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="b4412-103">Creating Embedded Objects</span></span>

<span data-ttu-id="b4412-104">Ao criar uma instância com objetos inseridos, execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b4412-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="b4412-105">Você deve declarar um objeto inserido como fortemente tipado ou com tipo fraco.</span><span class="sxs-lookup"><span data-stu-id="b4412-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="b4412-106">Um objeto fortemente tipado aponta para um objeto de uma classe específica e usa o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="b4412-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="b4412-107">Um objeto de tipo fraco aponta para um objeto de uma classe não especificada e usa a palavra-chave **Object** .</span><span class="sxs-lookup"><span data-stu-id="b4412-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="b4412-108">Ambos os objetos são mapeados para o tipo de **VT \_ desconhecido** .</span><span class="sxs-lookup"><span data-stu-id="b4412-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="b4412-109">Você pode usar **NULL** para o valor padrão de caminhos e objetos inseridos em inicializações e declarações.</span><span class="sxs-lookup"><span data-stu-id="b4412-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="b4412-110">Ao inserir um caminho de objeto, não coloque o espaço em branco entre os elementos do caminho inserido.</span><span class="sxs-lookup"><span data-stu-id="b4412-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="b4412-111">Por exemplo, o caminho do objeto "Class1Index = 3;" não contém espaço entre o nome da propriedade "Class1index" e o valor que está sendo atribuído, que é "3".</span><span class="sxs-lookup"><span data-stu-id="b4412-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="b4412-112">A declaração de classe a seguir mostra como declarar objetos embutidos fortemente tipados e com tipo fraco.</span><span class="sxs-lookup"><span data-stu-id="b4412-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="b4412-113">Os exemplos a seguir descrevem como declarar objetos incorporados dentro de uma declaração de classe.</span><span class="sxs-lookup"><span data-stu-id="b4412-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

<span data-ttu-id="b4412-114">O exemplo a seguir descreve a inicialização de uma propriedade que é um objeto fortemente tipado e outra propriedade que é uma matriz de objetos de tipo fraco.</span><span class="sxs-lookup"><span data-stu-id="b4412-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



