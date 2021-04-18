---
title: Estados do item de controle de guia (CommCtrl. h)
description: Os itens de controle de guia agora dão suporte a um estado de item para dar suporte à \_ mensagem TCM DESELECTALL. Além disso, a estrutura TCITEM dá suporte a valores de estado do item.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756023"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="e8534-104">Estados do item de controle de guia</span><span class="sxs-lookup"><span data-stu-id="e8534-104">Tab Control Item States</span></span>

<span data-ttu-id="e8534-105">Os itens de controle de guia agora dão suporte a um estado de item para dar suporte à mensagem [**TCM \_ DESELECTALL**](tcm-deselectall.md) .</span><span class="sxs-lookup"><span data-stu-id="e8534-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="e8534-106">Além disso, a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) dá suporte a valores de estado do item.</span><span class="sxs-lookup"><span data-stu-id="e8534-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="e8534-107">Constante</span><span class="sxs-lookup"><span data-stu-id="e8534-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="e8534-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8534-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="e8534-109"><dt>**TCIS \_ ButtonPressed**</dt></span><span class="sxs-lookup"><span data-stu-id="e8534-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="e8534-110">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e8534-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="e8534-111">O item de controle guia é selecionado.</span><span class="sxs-lookup"><span data-stu-id="e8534-111">The tab control item is selected.</span></span> <span data-ttu-id="e8534-112">Esse Estado só será significativo se o sinalizador de estilo de [**\_ botões de TCS**](tab-control-styles.md) tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="e8534-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="e8534-113"><dt>**TCIS \_ realçado**</dt></span><span class="sxs-lookup"><span data-stu-id="e8534-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="e8534-114">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="e8534-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="e8534-115">O item de controle guia é realçado e a guia e o texto são desenhados usando a cor de realce atual.</span><span class="sxs-lookup"><span data-stu-id="e8534-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="e8534-116">Ao usar High-Color, essa será uma interpolação real, não uma cor dificada.</span><span class="sxs-lookup"><span data-stu-id="e8534-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e8534-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8534-117">Requirements</span></span>



| <span data-ttu-id="e8534-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8534-118">Requirement</span></span> | <span data-ttu-id="e8534-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e8534-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8534-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8534-120">Header</span></span><br/> | <dl> <span data-ttu-id="e8534-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8534-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





