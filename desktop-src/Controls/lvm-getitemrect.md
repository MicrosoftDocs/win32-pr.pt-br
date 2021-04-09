---
title: Mensagem de LVM_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador para todo ou parte de um item no modo de exibição atual. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemRect do ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Controles de LVM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009650"
---
# <a name="lvm_getitemrect-message"></a><span data-ttu-id="69b98-105">\_Mensagem GETITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="69b98-105">LVM\_GETITEMRECT message</span></span>

<span data-ttu-id="69b98-106">Recupera o retângulo delimitador para todo ou parte de um item no modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="69b98-106">Retrieves the bounding rectangle for all or part of an item in the current view.</span></span> <span data-ttu-id="69b98-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="69b98-107">You can send this message explicitly or by using the [**ListView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="69b98-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b98-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b98-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b98-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="69b98-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="69b98-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="69b98-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b98-112">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="69b98-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span> <span data-ttu-id="69b98-113">Quando a mensagem é enviada, o membro **à esquerda** dessa estrutura é usado para especificar a parte do item de exibição de lista do qual recuperar o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="69b98-113">When the message is sent, the **left** member of this structure is used to specify the portion of the list-view item from which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="69b98-114">Ele deve ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="69b98-114">It must be set to one of the following values:</span></span>



| <span data-ttu-id="69b98-115">Valor</span><span class="sxs-lookup"><span data-stu-id="69b98-115">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="69b98-116">Significado</span><span class="sxs-lookup"><span data-stu-id="69b98-116">Meaning</span></span>                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="69b98-117"><dt>**limites do LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69b98-117"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl>                   | <span data-ttu-id="69b98-118">Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="69b98-118">Returns the bounding rectangle of the entire item, including the icon and label.</span></span><br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="69b98-119"><dt>**ícone de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69b98-119"><dt>**LVIR\_ICON**</dt></span></span> </dl>                         | <span data-ttu-id="69b98-120">Retorna o retângulo delimitador do ícone ou ícone pequeno.</span><span class="sxs-lookup"><span data-stu-id="69b98-120">Returns the bounding rectangle of the icon or small icon.</span></span><br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="69b98-121"><dt>**rótulo de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="69b98-121"><dt>**LVIR\_LABEL**</dt></span></span> </dl>                      | <span data-ttu-id="69b98-122">Retorna o retângulo delimitador do texto do item.</span><span class="sxs-lookup"><span data-stu-id="69b98-122">Returns the bounding rectangle of the item text.</span></span><br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <span data-ttu-id="69b98-123"><dt>**LVIR \_ SELECTBOUNDS**</dt></span><span class="sxs-lookup"><span data-stu-id="69b98-123"><dt>**LVIR\_SELECTBOUNDS**</dt></span></span> </dl> | <span data-ttu-id="69b98-124">Retorna a União do ícone LVIR \_ e dos \_ retângulos de rótulo LVIR, mas exclui colunas na exibição de relatório.</span><span class="sxs-lookup"><span data-stu-id="69b98-124">Returns the union of the LVIR\_ICON and LVIR\_LABEL rectangles, but excludes columns in report view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b98-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69b98-125">Return value</span></span>

<span data-ttu-id="69b98-126">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="69b98-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b98-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b98-127">Requirements</span></span>



| <span data-ttu-id="69b98-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b98-128">Requirement</span></span> | <span data-ttu-id="69b98-129">Valor</span><span class="sxs-lookup"><span data-stu-id="69b98-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69b98-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b98-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69b98-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69b98-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69b98-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b98-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69b98-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69b98-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69b98-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69b98-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b98-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b98-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

