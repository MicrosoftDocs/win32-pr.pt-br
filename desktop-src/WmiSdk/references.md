---
description: A palavra-chave de referência MOF descreve um caminho de objeto e é mapeada para um \_ tipo de automação VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Referências (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829123"
---
# <a name="references-wmi"></a><span data-ttu-id="7b328-103">Referências (WMI)</span><span class="sxs-lookup"><span data-stu-id="7b328-103">References (WMI)</span></span>

<span data-ttu-id="7b328-104">A palavra-chave de **referência** MOF descreve um caminho de objeto e é mapeada para um \_ tipo de automação VT BSTR.</span><span class="sxs-lookup"><span data-stu-id="7b328-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="7b328-105">O caminho do objeto pode ser um caminho completo para um servidor e namespace, ou um caminho relativo para outro objeto no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="7b328-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="7b328-106">Você pode usar uma palavra-chave de **referência** para vincular duas ou mais classes juntas.</span><span class="sxs-lookup"><span data-stu-id="7b328-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="7b328-107">O WMI dá suporte a dois tipos de caminhos de objeto, que usam para definir caminhos gerais ou específicos dentro do WMI.</span><span class="sxs-lookup"><span data-stu-id="7b328-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="7b328-108">A principal finalidade da palavra chave de **referência** é reduzir o tempo de transporte e a codificação entre objetos que existem inteiramente dentro do repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="7b328-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="7b328-109">Você também pode usar a palavra chave de **referência** para criar uma associação entre duas classes.</span><span class="sxs-lookup"><span data-stu-id="7b328-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="7b328-110">Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="7b328-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="7b328-111">Se o item referenciado estiver localizado dentro do mesmo arquivo MOF, use um alias para inicializar o valor de **referência** .</span><span class="sxs-lookup"><span data-stu-id="7b328-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="7b328-112">Para obter mais informações, consulte [criando um alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="7b328-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="7b328-113">Quando uma palavra de chave de **referência** é aplicada a uma propriedade de chave, você pode distinguir referências de objeto pelo valor de cadeia de caracteres do objeto em vez de pelo valor de cancelamento referenciado.</span><span class="sxs-lookup"><span data-stu-id="7b328-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="7b328-114">O MOF dá suporte ao conceito de um caminho de objeto de tipo fraco e fortemente tipado.</span><span class="sxs-lookup"><span data-stu-id="7b328-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="7b328-115">Um caminho de objeto de tipo fraco aponta para um objeto de uma classe não especificada e usa a palavra-chave **ref** com a palavra-chave [Object](object.md) .</span><span class="sxs-lookup"><span data-stu-id="7b328-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="7b328-116">Um objeto fortemente tipado aponta para um objeto de uma classe específica e usa **ref** com o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="7b328-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="7b328-117">O exemplo a seguir descreve uma referência de **RefToAnyClass** de tipo fraco que pode apontar para qualquer instância de classe ou classe e uma referência de **RefToClassX** que pode apontar apenas para uma classe ou instância **ClassX** :</span><span class="sxs-lookup"><span data-stu-id="7b328-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="7b328-118">O exemplo a seguir descreve duas instâncias e um objeto de associação que faz referência às instâncias anteriores:</span><span class="sxs-lookup"><span data-stu-id="7b328-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



