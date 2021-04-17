---
title: Elemento AcceptServerName
description: Indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento Servernames (ServerValidationParameters). | Elemento AcceptServerName
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Elemento AcceptServerName EAPHost
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
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763481"
---
# <a name="acceptservername-element"></a><span data-ttu-id="d509b-105">Elemento AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="d509b-105">AcceptServerName element</span></span>

<span data-ttu-id="d509b-106">O elemento **AcceptServerName (EapType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**servernames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d509b-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="d509b-107">O elemento **AcceptServerName** é definido pelo elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d509b-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d509b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d509b-108">Remarks</span></span>

<span data-ttu-id="d509b-109">O elemento **AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="d509b-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d509b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d509b-110">Requirements</span></span>



| <span data-ttu-id="d509b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d509b-111">Requirement</span></span> | <span data-ttu-id="d509b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d509b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d509b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d509b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d509b-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d509b-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d509b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d509b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d509b-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d509b-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d509b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d509b-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d509b-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d509b-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d509b-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="d509b-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="d509b-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d509b-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d509b-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="d509b-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="d509b-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d509b-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d509b-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d509b-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d509b-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d509b-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d509b-125">Elementos do esquema eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d509b-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d509b-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="d509b-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





