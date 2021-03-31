---
title: Elemento UseWinLogonCredentials (EapType)
description: Saiba mais sobre o elemento UseWinLogonCredentials (EapType). Esse elemento controla o uso de credenciais Winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641867"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="8c771-105">Elemento UseWinLogonCredentials (EapType)</span><span class="sxs-lookup"><span data-stu-id="8c771-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="8c771-106">O elemento **UseWinLogonCredentials (EapType)** controla o uso das credenciais Winlogin.</span><span class="sxs-lookup"><span data-stu-id="8c771-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="8c771-107">O elemento **UseWinLogonCredentials** é definido pelo elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8c771-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c771-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c771-108">Remarks</span></span>

<span data-ttu-id="8c771-109">Se for TRUE, o EAP MS-CHAPv2 obterá as credenciais do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="8c771-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="8c771-110">Se for FALSE, o EAP MS-CHAPv2 obterá as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c771-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="8c771-111">O elemento **UseWinLogonCredentials (EapType)** é opcional.</span><span class="sxs-lookup"><span data-stu-id="8c771-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c771-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c771-112">Requirements</span></span>



| <span data-ttu-id="8c771-113">Função</span><span class="sxs-lookup"><span data-stu-id="8c771-113">Role</span></span> | <span data-ttu-id="8c771-114">Versões mínimas do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="8c771-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="8c771-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="8c771-115">Client</span></span><br/> | <span data-ttu-id="8c771-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c771-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c771-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="8c771-117">Server</span></span><br/> | <span data-ttu-id="8c771-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c771-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c771-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8c771-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c771-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="8c771-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8c771-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="8c771-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="8c771-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="8c771-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8c771-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="8c771-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="8c771-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="8c771-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="8c771-125">Esquema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="8c771-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





