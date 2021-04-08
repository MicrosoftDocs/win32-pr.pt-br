---
title: Mensagem de EM_GETUNDONAME (RichEdit. h)
description: O Microsoft rich edit 2,0 e posterior recupera o tipo da próxima ação de desfazer, se houver. Microsoft Rich Edit 1,0 não há suporte para essa mensagem.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Controles de EM_GETUNDONAME de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918881"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="43321-104">\_Mensagem em GETundoname</span><span class="sxs-lookup"><span data-stu-id="43321-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="43321-105">Microsoft rich edit 2,0 e posterior: recupera o tipo da próxima ação de desfazer, se houver.</span><span class="sxs-lookup"><span data-stu-id="43321-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="43321-106">Microsoft Rich Edit 1,0: não há suporte para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="43321-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="43321-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43321-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43321-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43321-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43321-109">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="43321-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="43321-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43321-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43321-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="43321-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43321-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43321-112">Return value</span></span>

<span data-ttu-id="43321-113">Se houver uma ação de desfazer, o valor retornado será um valor de enumeração [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica o tipo da próxima ação na fila de desfazer do controle.</span><span class="sxs-lookup"><span data-stu-id="43321-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="43321-114">Se não houver ações que possam ser desfeitas ou o tipo da próxima ação de desfazer for desconhecido, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="43321-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="43321-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="43321-115">Remarks</span></span>

<span data-ttu-id="43321-116">Os tipos de ações que podem ser desfeitas ou refeitos incluem operações de digitação, exclusão, arrastar, soltar, recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="43321-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="43321-117">Essas informações podem ser úteis para aplicativos que fornecem uma interface do usuário estendida para operações de desfazer e refazer, como uma caixa de listagem suspensa de ações que podem ser desfeitas.</span><span class="sxs-lookup"><span data-stu-id="43321-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="43321-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43321-118">Requirements</span></span>



| <span data-ttu-id="43321-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43321-119">Requirement</span></span> | <span data-ttu-id="43321-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43321-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43321-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43321-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43321-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43321-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43321-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43321-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43321-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43321-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43321-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43321-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43321-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="43321-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43321-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43321-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="43321-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="43321-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43321-129">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="43321-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="43321-130">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="43321-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="43321-131">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="43321-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="43321-132">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="43321-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





