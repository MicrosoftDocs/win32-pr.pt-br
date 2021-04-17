---
description: Especifica o nome e o tipo de uma rede sem fio.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Tipo complexo networkitemtype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782183"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="7679f-103">Tipo complexo networkitemtype</span><span class="sxs-lookup"><span data-stu-id="7679f-103">networkItemType Complex Type</span></span>

<span data-ttu-id="7679f-104">O tipo complexo networkitemtype especifica o nome e o tipo de uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="7679f-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7679f-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7679f-105">Child elements</span></span>



| <span data-ttu-id="7679f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7679f-106">Element</span></span>                                                                      | <span data-ttu-id="7679f-107">Type</span><span class="sxs-lookup"><span data-stu-id="7679f-107">Type</span></span>                                                                    | <span data-ttu-id="7679f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7679f-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="7679f-109">**networkName**</span><span class="sxs-lookup"><span data-stu-id="7679f-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="7679f-110">**networkNameType**</span><span class="sxs-lookup"><span data-stu-id="7679f-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="7679f-111">O SSID (identificador de conjunto de serviços) da rede.</span><span class="sxs-lookup"><span data-stu-id="7679f-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="7679f-112">**NetworkType**</span><span class="sxs-lookup"><span data-stu-id="7679f-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="7679f-113">**networkTypeType**</span><span class="sxs-lookup"><span data-stu-id="7679f-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="7679f-114">O tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="7679f-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="7679f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7679f-115">Requirements</span></span>



| <span data-ttu-id="7679f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7679f-116">Requirement</span></span> | <span data-ttu-id="7679f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7679f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7679f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7679f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7679f-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7679f-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7679f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7679f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7679f-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7679f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




