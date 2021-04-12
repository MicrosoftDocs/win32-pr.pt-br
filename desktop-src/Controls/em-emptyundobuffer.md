---
title: Mensagem de EM_EMPTYUNDOBUFFER (WinUser. h)
description: Redefine o sinalizador de desfazer de um controle de edição. O sinalizador de desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Controles de EM_EMPTYUNDOBUFFER de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455442"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="a03f7-106">\_Mensagem em EMPTYUNDOBUFFER</span><span class="sxs-lookup"><span data-stu-id="a03f7-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="a03f7-107">Redefine o sinalizador de desfazer de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="a03f7-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="a03f7-108">O sinalizador de desfazer é definido sempre que uma operação dentro do controle de edição pode ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="a03f7-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="a03f7-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="a03f7-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a03f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a03f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a03f7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a03f7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a03f7-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a03f7-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a03f7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a03f7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a03f7-114">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a03f7-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a03f7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a03f7-115">Return value</span></span>

<span data-ttu-id="a03f7-116">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a03f7-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a03f7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a03f7-117">Remarks</span></span>

<span data-ttu-id="a03f7-118">O sinalizador de desfazer é redefinido automaticamente sempre que o controle de edição recebe uma mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) ou em [**\_ SetHandle**](em-sethandle.md) .</span><span class="sxs-lookup"><span data-stu-id="a03f7-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="a03f7-119">**Editar controles e edição avançada 1,0:** O controle só pode desfazer ou refazer a operação mais recente.</span><span class="sxs-lookup"><span data-stu-id="a03f7-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="a03f7-120">**Edição avançada 2,0 e posterior:** A mensagem em **\_ EMPTYUNDOBUFFER** esvazia todos os buffers de desfazer e refazer.</span><span class="sxs-lookup"><span data-stu-id="a03f7-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="a03f7-121">Os controles de edição avançados permitem que o usuário desfaça ou refaça várias operações.</span><span class="sxs-lookup"><span data-stu-id="a03f7-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="a03f7-122">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a03f7-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a03f7-123">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a03f7-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a03f7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a03f7-124">Requirements</span></span>



| <span data-ttu-id="a03f7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a03f7-125">Requirement</span></span> | <span data-ttu-id="a03f7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a03f7-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03f7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a03f7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a03f7-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a03f7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a03f7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a03f7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a03f7-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a03f7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a03f7-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a03f7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a03f7-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a03f7-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a03f7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a03f7-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="a03f7-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a03f7-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a03f7-135">**em \_ CANcelamento**</span><span class="sxs-lookup"><span data-stu-id="a03f7-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="a03f7-136">**\_ONhandle**</span><span class="sxs-lookup"><span data-stu-id="a03f7-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="a03f7-137">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="a03f7-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="a03f7-138">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="a03f7-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a03f7-139">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a03f7-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

