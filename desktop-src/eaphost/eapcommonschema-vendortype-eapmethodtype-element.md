---
title: Elemento Vendor (EapMethodType)
description: Saiba mais sobre o elemento Vendor (EapMethodType). Esse elemento é o tipo definido pelo fornecedor para o método.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorID do Vendor
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454340"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="10602-105">Elemento Vendor (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="10602-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="10602-106">O elemento **Vendor (EapMethodType)** é o tipo definido pelo fornecedor para o método.</span><span class="sxs-lookup"><span data-stu-id="10602-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="10602-107">O elemento **VendorID** é opcional.</span><span class="sxs-lookup"><span data-stu-id="10602-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="10602-108">Se usado, o **VendorName** é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="10602-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="10602-109">O elemento **VendorID** é definido pelo tipo complexo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="10602-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="10602-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10602-110">Requirements</span></span>



| <span data-ttu-id="10602-111">Função</span><span class="sxs-lookup"><span data-stu-id="10602-111">Role</span></span> | <span data-ttu-id="10602-112">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="10602-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="10602-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="10602-113">Client</span></span><br/> | <span data-ttu-id="10602-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10602-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10602-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="10602-115">Server</span></span><br/> | <span data-ttu-id="10602-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10602-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10602-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="10602-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="10602-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="10602-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="10602-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="10602-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="10602-120">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="10602-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="10602-121">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="10602-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





