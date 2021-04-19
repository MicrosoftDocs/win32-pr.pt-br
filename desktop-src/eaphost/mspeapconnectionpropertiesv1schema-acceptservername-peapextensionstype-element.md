---
title: Elemento AcceptServerName (PeapExtensionsType) (EAPHost)
description: Indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento Servernames (ServerValidationParameters). | Elemento AcceptServerName (PeapExtensionsType)
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
ms.openlocfilehash: ba4874b7c8761f35fa93387b23eaf5463a31bcf4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314599"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="f1af3-105">Elemento AcceptServerName (PeapExtensionsType) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="f1af3-105">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="f1af3-106">O elemento **AcceptServerName (PeapExtensionsType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**servernames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1af3-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="f1af3-107">O elemento é definido pelo elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f1af3-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1af3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1af3-108">Remarks</span></span>

<span data-ttu-id="f1af3-109">O elemento **AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="f1af3-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1af3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1af3-110">Requirements</span></span>



| <span data-ttu-id="f1af3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1af3-111">Requirement</span></span> | <span data-ttu-id="f1af3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f1af3-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f1af3-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1af3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f1af3-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f1af3-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f1af3-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1af3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f1af3-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f1af3-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1af3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1af3-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1af3-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="f1af3-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f1af3-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="f1af3-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f1af3-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="f1af3-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f1af3-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="f1af3-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f1af3-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f1af3-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f1af3-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="f1af3-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f1af3-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f1af3-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f1af3-125">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f1af3-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f1af3-126">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="f1af3-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





