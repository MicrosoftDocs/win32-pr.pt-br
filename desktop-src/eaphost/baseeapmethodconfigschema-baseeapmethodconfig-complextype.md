---
title: Tipo complexo BaseEapMethodConfig
description: Saiba mais sobre o tipo complexo BaseEapMethodConfig. Esse tipo é um elemento de espaço reservado para a configuração do método.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig tipo complexo EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366729"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="e2a32-105">Tipo complexo BaseEapMethodConfig</span><span class="sxs-lookup"><span data-stu-id="e2a32-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="e2a32-106">O tipo complexo **BaseEapMethodConfig** é um elemento de espaço reservado para a configuração do método.</span><span class="sxs-lookup"><span data-stu-id="e2a32-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="e2a32-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2a32-107">Remarks</span></span>

<span data-ttu-id="e2a32-108">O método EAP executa a validação de esquema no conteúdo do elemento **BaseEapMethodConfig** .</span><span class="sxs-lookup"><span data-stu-id="e2a32-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a32-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a32-109">Requirements</span></span>



| <span data-ttu-id="e2a32-110">Função</span><span class="sxs-lookup"><span data-stu-id="e2a32-110">Role</span></span> | <span data-ttu-id="e2a32-111">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a32-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="e2a32-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="e2a32-112">Client</span></span><br/> | <span data-ttu-id="e2a32-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2a32-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2a32-114">Servidor</span><span class="sxs-lookup"><span data-stu-id="e2a32-114">Server</span></span><br/> | <span data-ttu-id="e2a32-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2a32-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2a32-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2a32-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a32-117">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="e2a32-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e2a32-118">Esquema baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="e2a32-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





