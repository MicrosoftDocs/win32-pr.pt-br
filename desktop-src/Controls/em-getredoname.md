---
title: Mensagem de EM_GETREDONAME (RichEdit. h)
description: Recupera o tipo da próxima ação, se houver, na fila de restauração do controle de edição avançada.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Controles de EM_GETREDONAME de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918561"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="d70f4-104">\_Mensagem em refazer</span><span class="sxs-lookup"><span data-stu-id="d70f4-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="d70f4-105">Recupera o tipo da próxima ação, se houver, na fila de restauração do controle de edição avançada.</span><span class="sxs-lookup"><span data-stu-id="d70f4-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="d70f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d70f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d70f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d70f4-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d70f4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d70f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d70f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d70f4-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d70f4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d70f4-111">Return value</span></span>

<span data-ttu-id="d70f4-112">Se a fila de restauração do controle não estiver vazia, o valor retornado será um valor de enumeração [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica o tipo da próxima ação na fila de restauração do controle.</span><span class="sxs-lookup"><span data-stu-id="d70f4-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="d70f4-113">Se não houver ações refazêveis ou o tipo da próxima ação refeita for desconhecido, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="d70f4-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d70f4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d70f4-114">Remarks</span></span>

<span data-ttu-id="d70f4-115">Os tipos de ações que podem ser desfeitas ou refeitos incluem as operações de digitação, exclusão, arrastar e soltar, recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="d70f4-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="d70f4-116">Essas informações podem ser úteis para aplicativos que fornecem uma interface do usuário estendida para operações de desfazer e refazer, como uma caixa de listagem suspensa de ações refazêveis.</span><span class="sxs-lookup"><span data-stu-id="d70f4-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70f4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d70f4-117">Requirements</span></span>



| <span data-ttu-id="d70f4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70f4-118">Requirement</span></span> | <span data-ttu-id="d70f4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d70f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d70f4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d70f4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d70f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d70f4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d70f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d70f4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d70f4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d70f4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d70f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d70f4-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70f4-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d70f4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d70f4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d70f4-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d70f4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d70f4-128">**em \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="d70f4-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="d70f4-129">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="d70f4-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="d70f4-130">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="d70f4-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="d70f4-131">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="d70f4-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





