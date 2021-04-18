---
title: Categorizando por recursos de componente
description: As categorias de componentes podem ser usadas para exibir um subconjunto de todos os componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771274"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="f5b38-103">Categorizando por recursos de componente</span><span class="sxs-lookup"><span data-stu-id="f5b38-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="f5b38-104">As categorias de componentes podem ser usadas para exibir um subconjunto de todos os componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="f5b38-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="f5b38-105">Cada categoria de componente é identificada por um GUID, chamado de CATID (ID de categoria).</span><span class="sxs-lookup"><span data-stu-id="f5b38-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="f5b38-106">Cada CATID tem uma lista de nomes com marca de localidade e legíveis para pessoas associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="f5b38-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="f5b38-107">Uma lista das CATIDs e dos nomes legíveis é armazenada em um local conhecido no registro.</span><span class="sxs-lookup"><span data-stu-id="f5b38-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="f5b38-108">Por exemplo, todos os componentes que implementam a funcionalidade para inserção de documentos OLE podem ser classificados dentro de uma categoria de componente.</span><span class="sxs-lookup"><span data-stu-id="f5b38-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="f5b38-109">No passado, esses objetos teriam sido identificados pela chave "Insertable" no registro.</span><span class="sxs-lookup"><span data-stu-id="f5b38-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="f5b38-110">Para usar categorias de componente em vez disso, as seguintes informações seriam adicionadas ao registro:</span><span class="sxs-lookup"><span data-stu-id="f5b38-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="f5b38-111">Cada classe que implementa a funcionalidade correspondente a uma categoria de componente lista a ID de categoria para essa categoria dentro da chave de CLSID no registro.</span><span class="sxs-lookup"><span data-stu-id="f5b38-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="f5b38-112">Como um único componente pode dar suporte a uma ampla gama de funcionalidades, os componentes podem pertencer a várias categorias de componentes.</span><span class="sxs-lookup"><span data-stu-id="f5b38-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="f5b38-113">Por exemplo, um controle OLE específico pode dar suporte a toda a funcionalidade necessária para participar como incorporação de documentos OLE, vinculação de dados do Microsoft Visual Basic e funcionalidade de Internet.</span><span class="sxs-lookup"><span data-stu-id="f5b38-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="f5b38-114">Tal controle teria as seguintes informações armazenadas em sua chave CLSID no registro:</span><span class="sxs-lookup"><span data-stu-id="f5b38-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="f5b38-115">Com essas informações, um contêiner pode enumerar os controles instalados em um sistema e exibir somente os controles que dão suporte à funcionalidade exigida pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="f5b38-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="f5b38-116">O uso de categorias de componentes fornece uma maneira de categorizar componentes pela funcionalidade implementada do componente.</span><span class="sxs-lookup"><span data-stu-id="f5b38-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5b38-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5b38-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5b38-118">Associando ícones a uma categoria</span><span class="sxs-lookup"><span data-stu-id="f5b38-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="f5b38-119">Categorizando por recursos de contêiner</span><span class="sxs-lookup"><span data-stu-id="f5b38-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="f5b38-120">Classes e associações padrão</span><span class="sxs-lookup"><span data-stu-id="f5b38-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="f5b38-121">Definindo categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="f5b38-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="f5b38-122">O Gerenciador de categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="f5b38-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




