---
title: Elemento AuthorId (EapMethodType)
description: Saiba mais sobre o elemento AuthorId (EapMethodType). O elemento AuthorId (EapMethodType) refere-se ao autor do método.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento AuthorId EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917687"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="5029c-105">Elemento AuthorId (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="5029c-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="5029c-106">O elemento **AuthorId (EapMethodType)** refere-se ao autor do método.</span><span class="sxs-lookup"><span data-stu-id="5029c-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="5029c-107">O AuthorId é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="5029c-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="5029c-108">O elemento **AuthorId** é definido pelo tipo complexo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5029c-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5029c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5029c-109">Remarks</span></span>

<span data-ttu-id="5029c-110">Os elementos **AuthorId** e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) não precisam ser os mesmos para um método específico.</span><span class="sxs-lookup"><span data-stu-id="5029c-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5029c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5029c-111">Requirements</span></span>



| <span data-ttu-id="5029c-112">Função</span><span class="sxs-lookup"><span data-stu-id="5029c-112">Role</span></span> | <span data-ttu-id="5029c-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="5029c-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="5029c-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="5029c-114">Client</span></span><br/> | <span data-ttu-id="5029c-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5029c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5029c-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="5029c-116">Server</span></span><br/> | <span data-ttu-id="5029c-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5029c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5029c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5029c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5029c-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="5029c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5029c-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="5029c-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="5029c-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="5029c-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5029c-122">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="5029c-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





