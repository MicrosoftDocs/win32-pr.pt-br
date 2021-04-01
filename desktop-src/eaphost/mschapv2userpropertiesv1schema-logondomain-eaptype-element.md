---
title: Elemento LogonDomain (EapType)
description: Saiba mais sobre o elemento LogonDomain (EapType). Esse elemento identifica o domínio do usuário ou computador que está sendo autenticado.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008352"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="66cc1-105">Elemento LogonDomain (EapType)</span><span class="sxs-lookup"><span data-stu-id="66cc1-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="66cc1-106">O elemento **LogonDomain (EapType)** identifica o domínio do usuário ou computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="66cc1-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="66cc1-107">O elemento **LogonDomain** é definido pelo elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="66cc1-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="66cc1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="66cc1-108">Remarks</span></span>

<span data-ttu-id="66cc1-109">Se o elemento **LogonDomain (EapType)** não estiver presente, o domínio do Winlogon será usado.</span><span class="sxs-lookup"><span data-stu-id="66cc1-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="66cc1-110">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="66cc1-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cc1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66cc1-111">Requirements</span></span>



| <span data-ttu-id="66cc1-112">Função</span><span class="sxs-lookup"><span data-stu-id="66cc1-112">Role</span></span> | <span data-ttu-id="66cc1-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="66cc1-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="66cc1-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="66cc1-114">Client</span></span><br/> | <span data-ttu-id="66cc1-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66cc1-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="66cc1-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="66cc1-116">Server</span></span><br/> | <span data-ttu-id="66cc1-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66cc1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66cc1-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="66cc1-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="66cc1-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="66cc1-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66cc1-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="66cc1-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="66cc1-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="66cc1-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66cc1-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="66cc1-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="66cc1-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="66cc1-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="66cc1-124">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="66cc1-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





