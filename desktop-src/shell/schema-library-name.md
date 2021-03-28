---
description: O <name> elemento Especifica o nome dessa biblioteca. Esse elemento é necessário e não tem atributos ou elementos filho.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Elemento Name (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989107"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="ced31-104">Elemento Name (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="ced31-104">name Element (Library Schema)</span></span>

<span data-ttu-id="ced31-105">O <name> elemento Especifica o nome dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ced31-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="ced31-106">Esse elemento é necessário e não tem atributos ou elementos filho.</span><span class="sxs-lookup"><span data-stu-id="ced31-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ced31-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="ced31-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ced31-108">Element Information</span></span>



| <span data-ttu-id="ced31-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="ced31-109">Parent Element</span></span>                                                               | <span data-ttu-id="ced31-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ced31-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="ced31-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="ced31-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="ced31-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ced31-112">Remarks</span></span>

<span data-ttu-id="ced31-113">O nome é o nome da biblioteca amigável que é exibido no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="ced31-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="ced31-114">O nome pode ser especificado em um <dllname> <index> formato, como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ced31-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="ced31-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ced31-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ced31-116">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="ced31-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="ced31-117">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="ced31-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
