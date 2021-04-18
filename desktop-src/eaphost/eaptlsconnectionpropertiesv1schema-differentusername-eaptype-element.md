---
title: Elemento DifferentUsername (EapType)
description: Saiba mais sobre o elemento DifferentUsername (EapType). Esse elemento determina o nome de usuário que o EAP-TLS deve usar.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105781655"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="64f02-105">Elemento DifferentUsername (EapType)</span><span class="sxs-lookup"><span data-stu-id="64f02-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="64f02-106">O elemento **DifferentUsername (EapType)** determina o nome de usuário que o EAP-TLS deve usar.</span><span class="sxs-lookup"><span data-stu-id="64f02-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="64f02-107">O elemento **DifferentUsername** é definido pelo elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="64f02-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f02-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="64f02-108">Remarks</span></span>

<span data-ttu-id="64f02-109">Se o elemento **DifferentUserName** for true, o EAP-TLS deverá usar um nome de usuário diferente do nome que aparece no certificado.</span><span class="sxs-lookup"><span data-stu-id="64f02-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="64f02-110">Se o elemento **DifferentUserName** for false, o EAP-TLS usará o nome de usuário que aparece no certificado.</span><span class="sxs-lookup"><span data-stu-id="64f02-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="64f02-111">O elemento **DifferentUserName** é opcional.</span><span class="sxs-lookup"><span data-stu-id="64f02-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f02-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64f02-112">Requirements</span></span>



| <span data-ttu-id="64f02-113">Função</span><span class="sxs-lookup"><span data-stu-id="64f02-113">Role</span></span> | <span data-ttu-id="64f02-114">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="64f02-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="64f02-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="64f02-115">Client</span></span><br/> | <span data-ttu-id="64f02-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64f02-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64f02-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="64f02-117">Server</span></span><br/> | <span data-ttu-id="64f02-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64f02-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64f02-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="64f02-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="64f02-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="64f02-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="64f02-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="64f02-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="64f02-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="64f02-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="64f02-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="64f02-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="64f02-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="64f02-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="64f02-125">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="64f02-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="64f02-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="64f02-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="64f02-127">Elementos do esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="64f02-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





