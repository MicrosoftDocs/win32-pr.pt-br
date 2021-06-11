---
title: Elemento AcceptServerName (PeapExtensionsType) (EAPHost)
description: O elemento AcceptServerName (PeapExtensionsType) indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no esquema ServerNames no esquema mspeapconnectionpropertiesv1.
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989086"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="f3ba8-104">Elemento AcceptServerName (PeapExtensionsType) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="f3ba8-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="f3ba8-105">O **elemento AcceptServerName (PeapExtensionsType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="f3ba8-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="f3ba8-106">O elemento é definido pelo [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="f3ba8-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3ba8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3ba8-107">Remarks</span></span>

<span data-ttu-id="f3ba8-108">O **elemento AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="f3ba8-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3ba8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3ba8-109">Requirements</span></span>



| <span data-ttu-id="f3ba8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3ba8-110">Requirement</span></span> | <span data-ttu-id="f3ba8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f3ba8-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f3ba8-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3ba8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f3ba8-113">Somente aplicativos \[ da área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3ba8-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f3ba8-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3ba8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f3ba8-115">Somente aplicativos da área de trabalho do Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="f3ba8-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3ba8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3ba8-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3ba8-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f3ba8-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f3ba8-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="f3ba8-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f3ba8-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f3ba8-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f3ba8-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="f3ba8-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f3ba8-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f3ba8-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f3ba8-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f3ba8-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f3ba8-123">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f3ba8-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f3ba8-124">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f3ba8-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f3ba8-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="f3ba8-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





