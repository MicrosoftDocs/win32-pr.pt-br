---
description: Define uma lista que contém até cinco atributos de contador.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Tipo complexo de atributos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921737"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="838a5-103">Tipo complexo de atributos</span><span class="sxs-lookup"><span data-stu-id="838a5-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="838a5-104">Define uma lista que contém até cinco atributos de contador.</span><span class="sxs-lookup"><span data-stu-id="838a5-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="838a5-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="838a5-105">Child elements</span></span>



| <span data-ttu-id="838a5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="838a5-106">Element</span></span>              | <span data-ttu-id="838a5-107">Type</span><span class="sxs-lookup"><span data-stu-id="838a5-107">Type</span></span>                                                                               | <span data-ttu-id="838a5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="838a5-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="838a5-109">**Atributo myAttribute**</span><span class="sxs-lookup"><span data-stu-id="838a5-109">**counterAttribute**</span></span> | [<span data-ttu-id="838a5-110">**homem: Atributoy**</span><span class="sxs-lookup"><span data-stu-id="838a5-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="838a5-111">Um atributo de contador que especifica como os dados do contador são exibidos em um aplicativo de consumidor.</span><span class="sxs-lookup"><span data-stu-id="838a5-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="838a5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="838a5-112">Requirements</span></span>



| <span data-ttu-id="838a5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="838a5-113">Requirement</span></span> | <span data-ttu-id="838a5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="838a5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="838a5-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="838a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="838a5-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="838a5-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="838a5-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="838a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="838a5-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="838a5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




