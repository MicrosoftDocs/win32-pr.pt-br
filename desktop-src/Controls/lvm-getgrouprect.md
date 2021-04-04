---
title: Mensagem de LVM_GETGROUPRECT (commctrl. h)
description: Obtém o retângulo de um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro GetGroupRect do ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Controles de LVM_GETGROUPRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918034"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="e89ec-105">\_Mensagem GETGROUPRECT LVM</span><span class="sxs-lookup"><span data-stu-id="e89ec-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="e89ec-106">Obtém o retângulo de um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="e89ec-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="e89ec-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetGroupRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .</span><span class="sxs-lookup"><span data-stu-id="e89ec-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e89ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e89ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e89ec-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e89ec-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e89ec-110">Especifica o Group by **iGroupId** (consulte a estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="e89ec-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="e89ec-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e89ec-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e89ec-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber informações sobre o grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e89ec-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="e89ec-113">O receptor da mensagem é responsável por definir os membros da estrutura com informações para o grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e89ec-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="e89ec-114">O processo de chamada é responsável por alocar memória para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="e89ec-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="e89ec-115">Defina o membro **superior** do [**Rect**](/previous-versions//dd162897(v=vs.85)) como um dos sinalizadores a seguir para especificar as coordenadas do retângulo a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="e89ec-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="e89ec-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e89ec-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="e89ec-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e89ec-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="e89ec-118"><dt>**grupo de LVGGR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e89ec-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="e89ec-119">Coordenadas de todo o grupo expandido.</span><span class="sxs-lookup"><span data-stu-id="e89ec-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="e89ec-120"><dt>**\_cabeçalho LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="e89ec-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="e89ec-121">Coordenadas do cabeçalho somente (grupo recolhido).</span><span class="sxs-lookup"><span data-stu-id="e89ec-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="e89ec-122"><dt>**rótulo de LVGGR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e89ec-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="e89ec-123">Somente coordenadas do rótulo.</span><span class="sxs-lookup"><span data-stu-id="e89ec-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="e89ec-124"><dt>**LVGGR \_ SUBSETLINK**</dt></span><span class="sxs-lookup"><span data-stu-id="e89ec-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="e89ec-125">Coordenadas somente do link de subconjunto (subconjunto de marcação).</span><span class="sxs-lookup"><span data-stu-id="e89ec-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="e89ec-126">Um controle de exibição de lista pode limitar o número de itens visíveis exibidos em cada grupo.</span><span class="sxs-lookup"><span data-stu-id="e89ec-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="e89ec-127">Um link é apresentado ao usuário para permitir que o usuário expanda o grupo.</span><span class="sxs-lookup"><span data-stu-id="e89ec-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="e89ec-128">Esse sinalizador retornará o retângulo delimitador do link do subconjunto se o grupo for um subconjunto (estado do grupo de LVGS \_ subconjuntos, consulte estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **estado** do membro).</span><span class="sxs-lookup"><span data-stu-id="e89ec-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="e89ec-129">Esse sinalizador é fornecido para que os aplicativos de acessibilidade possam localizar o link.</span><span class="sxs-lookup"><span data-stu-id="e89ec-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e89ec-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e89ec-130">Return value</span></span>

<span data-ttu-id="e89ec-131">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e89ec-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e89ec-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e89ec-132">Requirements</span></span>



| <span data-ttu-id="e89ec-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e89ec-133">Requirement</span></span> | <span data-ttu-id="e89ec-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e89ec-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e89ec-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e89ec-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e89ec-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e89ec-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e89ec-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e89ec-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e89ec-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e89ec-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e89ec-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e89ec-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89ec-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e89ec-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

