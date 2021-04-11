---
title: AcceptServerName
description: Indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento Servernames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172752"
---
# <a name="acceptservername"></a><span data-ttu-id="81b11-105">AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="81b11-105">AcceptServerName</span></span>

<span data-ttu-id="81b11-106">O elemento **AcceptServerName (EapType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**servernames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="81b11-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="81b11-107">O elemento é definido pelo elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="81b11-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="81b11-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="81b11-108">Remarks</span></span>

<span data-ttu-id="81b11-109">O elemento **AcceptServerName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="81b11-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b11-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b11-110">Requirements</span></span>



| <span data-ttu-id="81b11-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b11-111">Requirement</span></span> | <span data-ttu-id="81b11-112">Valor</span><span class="sxs-lookup"><span data-stu-id="81b11-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="81b11-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81b11-113">Minimum supported client</span></span><br/> | <span data-ttu-id="81b11-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="81b11-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="81b11-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81b11-115">Minimum supported server</span></span><br/> | <span data-ttu-id="81b11-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="81b11-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81b11-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="81b11-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="81b11-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="81b11-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="81b11-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="81b11-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="81b11-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="81b11-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="81b11-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="81b11-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="81b11-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="81b11-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="81b11-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="81b11-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="81b11-124">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="81b11-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="81b11-125">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="81b11-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="81b11-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="81b11-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





