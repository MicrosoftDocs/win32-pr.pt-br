---
title: EFFECTs. currentEffect
description: O atributo currentEffect especifica ou recupera a visualização atual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796429"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="2cd5f-104">EFFECTs. currentEffect</span><span class="sxs-lookup"><span data-stu-id="2cd5f-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="2cd5f-105">O atributo **currentEffect** especifica ou recupera a visualização atual.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="2cd5f-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2cd5f-106">Possible Values</span></span>

<span data-ttu-id="2cd5f-107">Este atributo é um **objeto** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="2cd5f-108">O valor padrão é a primeira visualização na ordem de criação.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="2cd5f-109">Se não houver visualizações criadas na capa, o padrão será a primeira visualização no registro.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd5f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cd5f-110">Remarks</span></span>

<span data-ttu-id="2cd5f-111">Você pode usar esse objeto para acessar visualizações personalizadas que você criou.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="2cd5f-112">Por exemplo, você pode expor uma propriedade por meio da interface **IDispatch** em sua visualização.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="2cd5f-113">Em seguida, você pode alterar o valor da propriedade de sua capa, tornando a visualização o efeito atual e, em seguida, usando o objeto **currentEffect** para definir um novo valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="2cd5f-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="2cd5f-114">Por exemplo, se sua visualização expõe uma propriedade chamada backgroundColor, o seguinte código JScript especifica um novo valor:</span><span class="sxs-lookup"><span data-stu-id="2cd5f-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="2cd5f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cd5f-115">Requirements</span></span>



| <span data-ttu-id="2cd5f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd5f-116">Requirement</span></span> | <span data-ttu-id="2cd5f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2cd5f-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2cd5f-118">Versão</span><span class="sxs-lookup"><span data-stu-id="2cd5f-118">Version</span></span><br/> | <span data-ttu-id="2cd5f-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2cd5f-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cd5f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cd5f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd5f-121">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="2cd5f-122">**EFFECTs. currentEffectTitle**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="2cd5f-123">**EFFECTs. currentEffectType**</span><span class="sxs-lookup"><span data-stu-id="2cd5f-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





