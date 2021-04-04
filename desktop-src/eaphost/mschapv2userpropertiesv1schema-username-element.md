---
title: Elemento username (CHAP)
description: Saiba mais sobre o elemento username, que identifica o usuário que está sendo autenticado. Consulte um exemplo de sintaxe e exiba recursos adicionais disponíveis.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Elemento username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917678"
---
# <a name="username-element-chap"></a><span data-ttu-id="7f29d-105">Elemento username (CHAP)</span><span class="sxs-lookup"><span data-stu-id="7f29d-105">Username element (CHAP)</span></span>

<span data-ttu-id="7f29d-106">O elemento **username** identifica o usuário que está sendo autenticado.</span><span class="sxs-lookup"><span data-stu-id="7f29d-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="7f29d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f29d-107">Remarks</span></span>

<span data-ttu-id="7f29d-108">Se o elemento **username** não estiver presente, o nome de usuário será obtido do Winlogon.</span><span class="sxs-lookup"><span data-stu-id="7f29d-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="7f29d-109">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="7f29d-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f29d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f29d-110">Requirements</span></span>



| <span data-ttu-id="7f29d-111">Função</span><span class="sxs-lookup"><span data-stu-id="7f29d-111">Role</span></span> | <span data-ttu-id="7f29d-112">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="7f29d-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="7f29d-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="7f29d-113">Client</span></span><br/> | <span data-ttu-id="7f29d-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f29d-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f29d-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="7f29d-115">Server</span></span><br/> | <span data-ttu-id="7f29d-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f29d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f29d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f29d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f29d-118">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="7f29d-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7f29d-119">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7f29d-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





