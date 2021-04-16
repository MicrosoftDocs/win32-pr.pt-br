---
title: Elemento Identity
description: Saiba mais sobre o elemento de identidade EAPHost. Esse elemento captura a identidade usada para autenticação.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Elemento Identity EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454355"
---
# <a name="identity-element"></a><span data-ttu-id="e0c86-105">Elemento Identity</span><span class="sxs-lookup"><span data-stu-id="e0c86-105">Identity Element</span></span>

<span data-ttu-id="e0c86-106">O elemento **Identity** captura a identidade usada para autenticação.</span><span class="sxs-lookup"><span data-stu-id="e0c86-106">The **Identity** element captures the identity used for authentication.</span></span>

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a><span data-ttu-id="e0c86-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0c86-107">Remarks</span></span>

<span data-ttu-id="e0c86-108">O elemento **Identity** é abstract; cada método deve definir e usar um elemento derivado nos documentos da instância.</span><span class="sxs-lookup"><span data-stu-id="e0c86-108">The **Identity** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c86-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0c86-109">Requirements</span></span>



| <span data-ttu-id="e0c86-110">Função</span><span class="sxs-lookup"><span data-stu-id="e0c86-110">Role</span></span> | <span data-ttu-id="e0c86-111">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="e0c86-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="e0c86-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="e0c86-112">Client</span></span><br/> | <span data-ttu-id="e0c86-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0c86-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0c86-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="e0c86-114">Server</span></span><br/> | <span data-ttu-id="e0c86-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0c86-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0c86-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0c86-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c86-117">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="e0c86-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e0c86-118">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e0c86-118">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





