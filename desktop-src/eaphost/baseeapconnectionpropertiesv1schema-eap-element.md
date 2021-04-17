---
title: Elemento EAP (Propriedades de conexão)
description: Saiba mais sobre o elemento EAP. Esse elemento captura o tipo de método selecionado e a configuração específica do método. | Elemento EAP (Propriedades de conexão)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Elemento EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105790506"
---
# <a name="eap-element-connection-properties"></a><span data-ttu-id="6a810-106">Elemento EAP (Propriedades de conexão)</span><span class="sxs-lookup"><span data-stu-id="6a810-106">Eap Element (connection properties)</span></span>

<span data-ttu-id="6a810-107">O elemento **EAP** captura o tipo de método selecionado e a configuração específica do método.</span><span class="sxs-lookup"><span data-stu-id="6a810-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="6a810-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a810-108">Remarks</span></span>

<span data-ttu-id="6a810-109">O método pode definir os elementos constituintes dentro do elemento **EAP** .</span><span class="sxs-lookup"><span data-stu-id="6a810-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="6a810-110">O método também executa a validação de esquema nos elementos no **EAP**.</span><span class="sxs-lookup"><span data-stu-id="6a810-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a810-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a810-111">Requirements</span></span>



| <span data-ttu-id="6a810-112">Função</span><span class="sxs-lookup"><span data-stu-id="6a810-112">Role</span></span> | <span data-ttu-id="6a810-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="6a810-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6a810-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="6a810-114">Client</span></span><br/> | <span data-ttu-id="6a810-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a810-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a810-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="6a810-116">Server</span></span><br/> | <span data-ttu-id="6a810-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a810-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a810-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a810-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a810-119">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="6a810-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6a810-120">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6a810-120">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





