---
title: Elemento EapType (Propriedades de usuário base)
description: Saiba mais sobre o elemento EapType. Esse elemento captura a configuração específica do método dentro do elemento EAP. | Elemento EapType (Propriedades de usuário base)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105766475"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="378b8-106">Elemento EapType (Propriedades de usuário base)</span><span class="sxs-lookup"><span data-stu-id="378b8-106">EapType element (base user properties)</span></span>

<span data-ttu-id="378b8-107">O elemento **EapType** captura a configuração específica do método dentro do elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="378b8-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="378b8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="378b8-108">Remarks</span></span>

<span data-ttu-id="378b8-109">O elemento **EapType** é abstrato; cada método deve definir e usar um elemento derivado nos documentos da instância.</span><span class="sxs-lookup"><span data-stu-id="378b8-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="378b8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378b8-110">Requirements</span></span>



| <span data-ttu-id="378b8-111">Função</span><span class="sxs-lookup"><span data-stu-id="378b8-111">Role</span></span> | <span data-ttu-id="378b8-112">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="378b8-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="378b8-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="378b8-113">Client</span></span><br/> | <span data-ttu-id="378b8-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="378b8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="378b8-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="378b8-115">Server</span></span><br/> | <span data-ttu-id="378b8-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="378b8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="378b8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="378b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378b8-118">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="378b8-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="378b8-119">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="378b8-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





