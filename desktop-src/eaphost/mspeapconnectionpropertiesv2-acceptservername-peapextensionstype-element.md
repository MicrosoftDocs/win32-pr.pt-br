---
title: Elemento AcceptServerName (PeapExtensionsType)
description: O elemento AcceptServerName (PeapExtensionsType) indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada em ServerNames no esquema mspeapconnectionpropertiesv2.
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
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989471"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="f2477-104">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="f2477-104">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="f2477-105">O **elemento AcceptServerName (PeapExtensionsType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="f2477-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="f2477-106">O **elemento AcceptServerName** é definido pelo [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="f2477-106">The **AcceptServerName** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2477-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2477-107">Remarks</span></span>

<span data-ttu-id="f2477-108">O **elemento AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="f2477-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2477-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2477-109">Requirements</span></span>



| <span data-ttu-id="f2477-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2477-110">Requirement</span></span> | <span data-ttu-id="f2477-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f2477-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f2477-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2477-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f2477-113">Somente aplicativos \[ da área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f2477-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f2477-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2477-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f2477-115">Somente aplicativos da área de trabalho do Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="f2477-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2477-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2477-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2477-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f2477-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f2477-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="f2477-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f2477-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f2477-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f2477-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="f2477-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f2477-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f2477-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f2477-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f2477-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f2477-123">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f2477-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f2477-124">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="f2477-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





