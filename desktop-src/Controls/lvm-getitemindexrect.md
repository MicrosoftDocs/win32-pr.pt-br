---
title: Mensagem de LVM_GETITEMINDEXRECT (commctrl. h)
description: Recupera o retângulo delimitador para todo ou parte de um subitem no modo de exibição atual de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetItemIndexRect do ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Controles de LVM_GETITEMINDEXRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455748"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="a5fa6-105">\_Mensagem GETITEMINDEXRECT LVM</span><span class="sxs-lookup"><span data-stu-id="a5fa6-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="a5fa6-106">Recupera o retângulo delimitador para todo ou parte de um subitem no modo de exibição atual de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="a5fa6-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetItemIndexRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .</span><span class="sxs-lookup"><span data-stu-id="a5fa6-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5fa6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5fa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5fa6-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa6-110">Um ponteiro para uma estrutura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para o item pai do subitem.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="a5fa6-111">O processo de chamada é responsável por alocar essa estrutura e definir seus membros.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="a5fa6-112">*wParam* não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a5fa6-113">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa6-114">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="a5fa6-115">O processo de chamada é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="a5fa6-116">*lParam* não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="a5fa6-117">Defina o membro **superior** como o índice do subitem.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="a5fa6-118">Defina o membro **esquerdo** como um dos valores a seguir, indicando a parte do subitem para o qual o retângulo delimitador será recuperado.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="a5fa6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a5fa6-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a5fa6-120">Significado</span><span class="sxs-lookup"><span data-stu-id="a5fa6-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="a5fa6-121"><dt>**limites do LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="a5fa6-122">Retorna o retângulo delimitador do subitem inteiro, incluindo o ícone e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="a5fa6-123"><dt>**ícone de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="a5fa6-124">Retorna o retângulo delimitador do ícone ou ícone pequeno do subitem.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="a5fa6-125"><dt>**rótulo de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="a5fa6-126">Retorna o retângulo delimitador do texto do subitem.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5fa6-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5fa6-127">Return value</span></span>

<span data-ttu-id="a5fa6-128">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fa6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5fa6-129">Requirements</span></span>



| <span data-ttu-id="a5fa6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5fa6-130">Requirement</span></span> | <span data-ttu-id="a5fa6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a5fa6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fa6-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fa6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fa6-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5fa6-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fa6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fa6-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5fa6-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5fa6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5fa6-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

