---
title: Elemento EapType (Propriedade de conexão de esquema v1)
description: Saiba mais sobre o elemento EapType. Esse elemento captura a configuração específica do método dentro do elemento EAP. | Elemento EapType (Propriedade de conexão de esquema v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663876"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="d2f0e-106">Elemento EapType (Propriedade de conexão de esquema v1)</span><span class="sxs-lookup"><span data-stu-id="d2f0e-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="d2f0e-107">O elemento **EapType** captura a configuração específica do método dentro do elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="d2f0e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2f0e-108">Remarks</span></span>

<span data-ttu-id="d2f0e-109">O elemento **EapType** é abstrato; cada método deve definir e usar um elemento derivado nos documentos da instância.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f0e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f0e-110">Requirements</span></span>



| <span data-ttu-id="d2f0e-111">Função</span><span class="sxs-lookup"><span data-stu-id="d2f0e-111">Role</span></span> | <span data-ttu-id="d2f0e-112">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="d2f0e-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d2f0e-113">Cliente</span><span class="sxs-lookup"><span data-stu-id="d2f0e-113">Client</span></span><br/> | <span data-ttu-id="d2f0e-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2f0e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d2f0e-115">Servidor</span><span class="sxs-lookup"><span data-stu-id="d2f0e-115">Server</span></span><br/> | <span data-ttu-id="d2f0e-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2f0e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2f0e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2f0e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f0e-118">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="d2f0e-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d2f0e-119">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d2f0e-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





