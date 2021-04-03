---
title: Elemento AcceptServerName (PeapExtensionsType)
description: Indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento Servernames (ServerValidationParameters). | Elemento AcceptServerName (PeapExtensionsType)
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d085122104c2764896801015c58fcbc9f72a1580
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930470"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="92bc8-105">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="92bc8-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="92bc8-106">O elemento **AcceptServerName (PeapExtensionsType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**servernames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="92bc8-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="92bc8-107">O elemento **AcceptServerName** é definido pelo elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="92bc8-107">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="92bc8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bc8-108">Remarks</span></span>

<span data-ttu-id="92bc8-109">O elemento **AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="92bc8-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="92bc8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bc8-110">Requirements</span></span>



| <span data-ttu-id="92bc8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bc8-111">Requirement</span></span> | <span data-ttu-id="92bc8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="92bc8-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="92bc8-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92bc8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="92bc8-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="92bc8-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="92bc8-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92bc8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="92bc8-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="92bc8-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92bc8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="92bc8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="92bc8-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="92bc8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="92bc8-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="92bc8-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="92bc8-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="92bc8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="92bc8-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="92bc8-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="92bc8-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="92bc8-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="92bc8-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="92bc8-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="92bc8-124">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="92bc8-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="92bc8-125">Elementos do esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="92bc8-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





