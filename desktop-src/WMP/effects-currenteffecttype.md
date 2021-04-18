---
title: EFFECTs. currentEffectType
description: O atributo currentEffectType especifica ou recupera o nome do registro da visualização atual. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760450"
---
# <a name="effectscurrenteffecttype"></a><span data-ttu-id="1ae6b-105">EFFECTs. currentEffectType</span><span class="sxs-lookup"><span data-stu-id="1ae6b-105">EFFECTS.currentEffectType</span></span>

<span data-ttu-id="1ae6b-106">O atributo **currentEffectType** especifica ou recupera o nome do registro da visualização atual.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-106">The **currentEffectType** attribute specifies or retrieves the registry name of the current visualization.</span></span> <span data-ttu-id="1ae6b-107">Esse nome é uma ID exclusiva definida pelo autor da visualização.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a><span data-ttu-id="1ae6b-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1ae6b-108">Possible Values</span></span>

<span data-ttu-id="1ae6b-109">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ae6b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ae6b-110">Remarks</span></span>

<span data-ttu-id="1ae6b-111">Você pode usar esse atributo em tempo de execução para alterar o efeito exibido no momento.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-111">You can use this attribute at run time to change the currently displayed effect.</span></span> <span data-ttu-id="1ae6b-112">Para fazer isso, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1ae6b-112">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="1ae6b-113">Use **effectCount** para recuperar a contagem de efeitos registrados.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-113">Use **effectCount** to retrieve the count of registered effects.</span></span>
2.  <span data-ttu-id="1ae6b-114">Em um loop, recupere o nome de cada efeito registrado usando **effecttype**.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-114">In a loop, retrieve the name of each registered effect by using **effectType**.</span></span>
3.  <span data-ttu-id="1ae6b-115">Especifique um dos nomes que você recuperou para **currentEffectType** para definir o efeito atual.</span><span class="sxs-lookup"><span data-stu-id="1ae6b-115">Specify one of the names you retrieved for **currentEffectType** to set the current effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae6b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ae6b-116">Requirements</span></span>



| <span data-ttu-id="1ae6b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae6b-117">Requirement</span></span> | <span data-ttu-id="1ae6b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1ae6b-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1ae6b-119">Versão</span><span class="sxs-lookup"><span data-stu-id="1ae6b-119">Version</span></span><br/> | <span data-ttu-id="1ae6b-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1ae6b-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ae6b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ae6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae6b-122">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="1ae6b-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="1ae6b-123">**EFFECTs. currentEffect**</span><span class="sxs-lookup"><span data-stu-id="1ae6b-123">**EFFECTS.currentEffect**</span></span>](effects-currenteffect.md)
</dt> <dt>

[<span data-ttu-id="1ae6b-124">**EFFECTs. effectCount**</span><span class="sxs-lookup"><span data-stu-id="1ae6b-124">**EFFECTS.effectCount**</span></span>](effects-effectcount.md)
</dt> <dt>

[<span data-ttu-id="1ae6b-125">**EFFECTs. effecttype**</span><span class="sxs-lookup"><span data-stu-id="1ae6b-125">**EFFECTS.effectType**</span></span>](effects-effecttype.md)
</dt> </dl>

 

 





