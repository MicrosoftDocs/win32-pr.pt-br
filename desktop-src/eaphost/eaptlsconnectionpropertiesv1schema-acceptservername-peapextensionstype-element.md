---
title: TLSExtensions (esquema v1)
description: Saiba mais sobre o elemento TLSExtensions (EapType). Esse elemento permite aprimoramentos futuros no esquema.
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105789925"
---
# <a name="tlsextensions-v1-schema"></a><span data-ttu-id="1b6a5-105">TLSExtensions (esquema v1)</span><span class="sxs-lookup"><span data-stu-id="1b6a5-105">TLSExtensions (v1 schema)</span></span>

<span data-ttu-id="1b6a5-106">O elemento **TLSExtensions (EapType)** permite aprimoramentos futuros no esquema.</span><span class="sxs-lookup"><span data-stu-id="1b6a5-106">The **TLSExtensions (EapType)** element enables future enhancements to the schema.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

<span data-ttu-id="1b6a5-107">O elemento é definido pelo elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1b6a5-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b6a5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b6a5-108">Remarks</span></span>

<span data-ttu-id="1b6a5-109">O elemento **TLSExtensions** é opcional.</span><span class="sxs-lookup"><span data-stu-id="1b6a5-109">The **TLSExtensions** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b6a5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b6a5-110">Requirements</span></span>



| <span data-ttu-id="1b6a5-111">Função</span><span class="sxs-lookup"><span data-stu-id="1b6a5-111">Role</span></span> | <span data-ttu-id="1b6a5-112">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="1b6a5-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="1b6a5-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="1b6a5-113">Client</span></span><br/> | <span data-ttu-id="1b6a5-114">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1b6a5-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1b6a5-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="1b6a5-115">Server</span></span><br/> | <span data-ttu-id="1b6a5-116">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="1b6a5-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b6a5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b6a5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b6a5-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="1b6a5-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1b6a5-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="1b6a5-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="1b6a5-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="1b6a5-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1b6a5-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="1b6a5-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="1b6a5-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1b6a5-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1b6a5-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="1b6a5-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1b6a5-124">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1b6a5-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1b6a5-125">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1b6a5-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1b6a5-126">**TLSExtensions (TLSExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="1b6a5-126">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





