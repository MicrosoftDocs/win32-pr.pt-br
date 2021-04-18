---
description: Um alias no WMI é uma referência simbólica em uma classe ou instância de classe localizada em outro lugar em um arquivo formato MOF (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Criando um alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814142"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="bc7b8-103">Criando um alias WMI</span><span class="sxs-lookup"><span data-stu-id="bc7b8-103">Creating a WMI Alias</span></span>

<span data-ttu-id="bc7b8-104">Um [*alias*](gloss-a.md) no WMI é uma referência simbólica em uma classe ou instância de classe localizada em outro lugar em um arquivo formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="bc7b8-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="bc7b8-105">O compilador MOF usa aliases para estabelecer referências entre classes e instâncias.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="bc7b8-106">O compilador resolve aliases para as classes às quais se referem, de modo que os nomes de alias não estão disponíveis no código compilado.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="bc7b8-107">Como resultado, os aplicativos cliente não podem se referir a classes que usam aliases.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="bc7b8-108">O WMI dá suporte à referência direta, mas não a aliases circulares.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="bc7b8-109">Um alias tem escopo somente dentro do arquivo MOF no qual você declara o alias.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="bc7b8-110">Portanto, normalmente você usa um alias como um atalho para um caminho de objeto longo.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="bc7b8-111">**Para definir um alias**</span><span class="sxs-lookup"><span data-stu-id="bc7b8-111">**To define an alias**</span></span>

1.  <span data-ttu-id="bc7b8-112">Adicione a frase "como $*aliasname*" à declaração de instância ou classe.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="bc7b8-113">Os nomes de alias seguem as mesmas regras que os nomes de instância e classe, exceto que os nomes de alias devem começar com um cifrão ($).</span><span class="sxs-lookup"><span data-stu-id="bc7b8-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="bc7b8-114">Sublinhados podem aparecer em um nome de alias após o caractere inicial.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="bc7b8-115">O exemplo de código a seguir descreve como usar um alias em uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="bc7b8-116">Os exemplos de código a seguir descrevem como usar um alias como uma referência simbólica para um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="bc7b8-117">Esses exemplos declaram duas classes para descrever um disco: a classe Disk para indicar a letra da unidade e a classe DiskRef para indicar o caminho do disco.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="bc7b8-118">Um alias é definido para a instância de classe de disco.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="bc7b8-119">Esse alias é usado como o valor para a propriedade PathToDisk na instância DiskRef.</span><span class="sxs-lookup"><span data-stu-id="bc7b8-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="bc7b8-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc7b8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc7b8-121">Criando uma classe</span><span class="sxs-lookup"><span data-stu-id="bc7b8-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



