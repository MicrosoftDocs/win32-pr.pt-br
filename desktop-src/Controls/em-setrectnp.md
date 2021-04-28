---
title: Mensagem de EM_SETRECTNP (WinUser. h)
description: EM_SETRECTNP mensagem – define o retângulo de formatação de um controle de edição de várias linhas.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Controles de EM_SETRECTNP de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085984"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="1ed49-104">\_Mensagem em SETRECTNP</span><span class="sxs-lookup"><span data-stu-id="1ed49-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="1ed49-105">Define o [retângulo de formatação](about-edit-controls.md) de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="1ed49-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="1ed49-106">A mensagem em **\_ SETRECTNP** é idêntica à mensagem [**em \_ SetRect**](em-setrect.md) , exceto que em **\_ SETRECTNP** *não* redesenha a janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1ed49-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="1ed49-107">O retângulo de formatação é o retângulo limitador no qual o controle desenha o texto.</span><span class="sxs-lookup"><span data-stu-id="1ed49-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="1ed49-108">O retângulo de limitação é independente do tamanho da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1ed49-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="1ed49-109">Essa mensagem é processada somente por controles de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="1ed49-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="1ed49-110">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1ed49-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ed49-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed49-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ed49-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ed49-113">**Edição avançada 3,0 e posterior:** Indica se o novo retângulo contém coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="1ed49-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="1ed49-114">Um valor de zero indica coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="1ed49-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="1ed49-115">Um valor de 1 indica deslocamentos relativos ao retângulo de formatação atual.</span><span class="sxs-lookup"><span data-stu-id="1ed49-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="1ed49-116">(Os deslocamentos podem ser positivos ou negativos.)</span><span class="sxs-lookup"><span data-stu-id="1ed49-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="1ed49-117">**Controles de edição:** Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ed49-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ed49-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ed49-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ed49-119">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica as novas dimensões do retângulo.</span><span class="sxs-lookup"><span data-stu-id="1ed49-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="1ed49-120">Se esse parâmetro for **NULL**, o retângulo de formatação será definido com seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="1ed49-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed49-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1ed49-121">Return value</span></span>

<span data-ttu-id="1ed49-122">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1ed49-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed49-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ed49-123">Remarks</span></span>

<span data-ttu-id="1ed49-124">**Edição avançada:** Com suporte no Microsoft Rich Edit 3,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1ed49-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="1ed49-125">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1ed49-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed49-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed49-126">Requirements</span></span>



| <span data-ttu-id="1ed49-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed49-127">Requirement</span></span> | <span data-ttu-id="1ed49-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed49-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed49-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed49-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed49-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ed49-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ed49-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ed49-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed49-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ed49-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ed49-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ed49-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed49-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ed49-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed49-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1ed49-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="1ed49-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1ed49-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ed49-137">**em \_ SETrect**</span><span class="sxs-lookup"><span data-stu-id="1ed49-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="1ed49-138">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="1ed49-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1ed49-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ed49-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

