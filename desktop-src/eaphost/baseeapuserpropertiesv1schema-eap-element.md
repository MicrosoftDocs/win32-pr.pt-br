---
title: Elemento EAP (Propriedade User)
description: Saiba mais sobre o elemento EAP. Esse elemento captura o tipo de método selecionado e a configuração específica do método. | Elemento EAP (Propriedade User)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
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
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105787740"
---
# <a name="eap-element-user-property"></a><span data-ttu-id="edffa-106">Elemento EAP (Propriedade User)</span><span class="sxs-lookup"><span data-stu-id="edffa-106">Eap element (user property)</span></span>

<span data-ttu-id="edffa-107">O elemento **EAP** captura o tipo de método selecionado e a configuração específica do método.</span><span class="sxs-lookup"><span data-stu-id="edffa-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="edffa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="edffa-108">Remarks</span></span>

<span data-ttu-id="edffa-109">O método pode definir os elementos constituintes dentro do elemento **EAP** .</span><span class="sxs-lookup"><span data-stu-id="edffa-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="edffa-110">O método também executa a validação de esquema nos elementos no **EAP**.</span><span class="sxs-lookup"><span data-stu-id="edffa-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="edffa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edffa-111">Requirements</span></span>



| <span data-ttu-id="edffa-112">Função</span><span class="sxs-lookup"><span data-stu-id="edffa-112">Role</span></span> | <span data-ttu-id="edffa-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="edffa-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="edffa-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="edffa-114">Client</span></span><br/> | <span data-ttu-id="edffa-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edffa-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="edffa-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="edffa-116">Server</span></span><br/> | <span data-ttu-id="edffa-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="edffa-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edffa-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="edffa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edffa-119">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="edffa-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="edffa-120">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="edffa-120">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





