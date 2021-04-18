---
title: Tipo complexo BaseEapParameters – Propriedades do usuário
description: Define o elemento que especificou o método herdado selecionado e as credenciais específicas do método.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105793832"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="990c2-104">Tipo complexo BaseEapParameters – Propriedades do usuário</span><span class="sxs-lookup"><span data-stu-id="990c2-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="990c2-105">O tipo complexo **BaseEapParameters** define o elemento que especificou o método herdado selecionado e as credenciais específicas do método.</span><span class="sxs-lookup"><span data-stu-id="990c2-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="990c2-106">O método pode definir os elementos constituintes dentro de **BaseEapParameters**; o método também executa a validação de esquema nos elementos no **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="990c2-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="990c2-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="990c2-107">Child elements</span></span>



| <span data-ttu-id="990c2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="990c2-108">Element</span></span>                                                                      | <span data-ttu-id="990c2-109">Type</span><span class="sxs-lookup"><span data-stu-id="990c2-109">Type</span></span>    | <span data-ttu-id="990c2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="990c2-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="990c2-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="990c2-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="990c2-112">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="990c2-112">integer</span></span> | <span data-ttu-id="990c2-113">Define o elemento de espaço reservado para o tipo de método selecionado e as credenciais específicas do método.</span><span class="sxs-lookup"><span data-stu-id="990c2-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="990c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="990c2-114">Requirements</span></span>



| <span data-ttu-id="990c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="990c2-115">Requirement</span></span> | <span data-ttu-id="990c2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="990c2-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="990c2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="990c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="990c2-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="990c2-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="990c2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="990c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="990c2-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="990c2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="990c2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="990c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="990c2-122">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="990c2-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="990c2-123">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="990c2-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





