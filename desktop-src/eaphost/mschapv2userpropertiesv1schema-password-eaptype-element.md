---
title: Elemento Password (EapType)
description: Saiba mais sobre o elemento Password (EapType). Esse elemento identifica a senha do usuário ou computador que está sendo autenticado.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008382"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="2150f-105">Elemento Password (EapType)</span><span class="sxs-lookup"><span data-stu-id="2150f-105">Password (EapType) Element</span></span>

<span data-ttu-id="2150f-106">O elemento **password (EapType)** identifica a senha do usuário ou computador que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="2150f-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="2150f-107">O elemento **password** é definido pelo elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2150f-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2150f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2150f-108">Remarks</span></span>

<span data-ttu-id="2150f-109">Se o elemento **password (EapType)** não estiver presente, o hash de senha será obtido do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="2150f-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="2150f-110">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="2150f-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2150f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2150f-111">Requirements</span></span>



| <span data-ttu-id="2150f-112">Função</span><span class="sxs-lookup"><span data-stu-id="2150f-112">Role</span></span> | <span data-ttu-id="2150f-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="2150f-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2150f-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="2150f-114">Client</span></span><br/> | <span data-ttu-id="2150f-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2150f-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2150f-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="2150f-116">Server</span></span><br/> | <span data-ttu-id="2150f-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2150f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2150f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2150f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2150f-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="2150f-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2150f-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="2150f-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="2150f-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="2150f-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2150f-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="2150f-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="2150f-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="2150f-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2150f-124">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2150f-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





