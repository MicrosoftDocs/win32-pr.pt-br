---
title: EFFECTs. allowAll
description: O atributo allowAll especifica ou recupera um valor que indica se todas as visualizações que estão no registro devem ser incluídas.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789561"
---
# <a name="effectsallowall"></a><span data-ttu-id="42d52-104">EFFECTs. allowAll</span><span class="sxs-lookup"><span data-stu-id="42d52-104">EFFECTS.allowAll</span></span>

<span data-ttu-id="42d52-105">O atributo **allowAll** especifica ou recupera um valor que indica se todas as visualizações que estão no registro devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="42d52-105">The **allowAll** attribute specifies or retrieves a value indicating whether to include all the visualizations that are in the registry.</span></span>

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a><span data-ttu-id="42d52-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="42d52-106">Possible Values</span></span>

<span data-ttu-id="42d52-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="42d52-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="42d52-108">Valor</span><span class="sxs-lookup"><span data-stu-id="42d52-108">Value</span></span> | <span data-ttu-id="42d52-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="42d52-109">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="42d52-110">true</span><span class="sxs-lookup"><span data-stu-id="42d52-110">true</span></span>  | <span data-ttu-id="42d52-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="42d52-111">Default.</span></span> <span data-ttu-id="42d52-112">Permite o ciclo de todas as visualizações no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="42d52-112">Allows cycling of all visualizations on the user's system.</span></span> |
| <span data-ttu-id="42d52-113">false</span><span class="sxs-lookup"><span data-stu-id="42d52-113">false</span></span> | <span data-ttu-id="42d52-114">Limita o ciclo às visualizações que aparecem dentro das marcas de **efeitos** .</span><span class="sxs-lookup"><span data-stu-id="42d52-114">Limits cycling to visualizations appearing within **EFFECTS** tags.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42d52-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="42d52-115">Remarks</span></span>

<span data-ttu-id="42d52-116">Se esse atributo for definido como false, somente as visualizações que aparecem dentro de marcas de **efeitos** podem ser alternadas usando Previous/avançar.</span><span class="sxs-lookup"><span data-stu-id="42d52-116">If this attribute is set to false, only the visualizations appearing within **EFFECTS** tags can be cycled through using previous/next.</span></span> <span data-ttu-id="42d52-117">Se estiver definido como true, todas as visualizações registradas no sistema do usuário poderão ser alternadas pelo.</span><span class="sxs-lookup"><span data-stu-id="42d52-117">If it is set to true, then all visualizations that are registered on the user's system can be cycled through.</span></span> <span data-ttu-id="42d52-118">Se ele for definido como true e você especificar quaisquer visualizações dentro de marcas de **efeitos** , os atributos especificados nessas marcas serão aplicados a todas as visualizações no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="42d52-118">If it is set to true and you specify any visualizations within **EFFECTS** tags, then the attributes specified in these tags are applied to all visualizations on the user's system.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d52-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d52-119">Requirements</span></span>



| <span data-ttu-id="42d52-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d52-120">Requirement</span></span> | <span data-ttu-id="42d52-121">Valor</span><span class="sxs-lookup"><span data-stu-id="42d52-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="42d52-122">Versão</span><span class="sxs-lookup"><span data-stu-id="42d52-122">Version</span></span><br/> | <span data-ttu-id="42d52-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="42d52-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42d52-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="42d52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d52-125">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="42d52-125">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





