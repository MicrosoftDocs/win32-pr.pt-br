---
title: Tipo complexo BaseEapParameters – Propriedades de conexão
description: Define o elemento de espaço reservado para o tipo de método e a configuração específica do método.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters tipo complexo EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105790507"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="7110f-104">Tipo complexo BaseEapParameters – Propriedades de conexão</span><span class="sxs-lookup"><span data-stu-id="7110f-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="7110f-105">O tipo complexo **BaseEapParameters** define o elemento de espaço reservado para o tipo de método e a configuração específica do método.</span><span class="sxs-lookup"><span data-stu-id="7110f-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7110f-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7110f-106">Child elements</span></span>



| <span data-ttu-id="7110f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7110f-107">Element</span></span>                                                                            | <span data-ttu-id="7110f-108">Type</span><span class="sxs-lookup"><span data-stu-id="7110f-108">Type</span></span>    | <span data-ttu-id="7110f-109">Description</span><span class="sxs-lookup"><span data-stu-id="7110f-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="7110f-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="7110f-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="7110f-111">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7110f-111">integer</span></span> | <span data-ttu-id="7110f-112">Qualquer instância de esquema é permitida aqui.</span><span class="sxs-lookup"><span data-stu-id="7110f-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7110f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7110f-113">Remarks</span></span>

<span data-ttu-id="7110f-114">Em **BaseEapParameters** , o método pode definir os elementos constituintes.</span><span class="sxs-lookup"><span data-stu-id="7110f-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="7110f-115">O método também executa a validação de esquema nos elementos no **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="7110f-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7110f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7110f-116">Requirements</span></span>



| <span data-ttu-id="7110f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7110f-117">Requirement</span></span> | <span data-ttu-id="7110f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7110f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7110f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7110f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7110f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7110f-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7110f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7110f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7110f-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7110f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7110f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7110f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7110f-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="7110f-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7110f-125">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7110f-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





