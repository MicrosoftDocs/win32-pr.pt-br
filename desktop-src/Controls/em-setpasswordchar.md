---
title: Mensagem de EM_SETPASSWORDCHAR (WinUser. h)
description: Define ou remove o caractere de senha para um controle de edição. Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Controles de EM_SETPASSWORDCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455019"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="32b0d-106">\_Mensagem em SETpasswordchar</span><span class="sxs-lookup"><span data-stu-id="32b0d-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="32b0d-107">Define ou remove o caractere de senha para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="32b0d-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="32b0d-108">Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="32b0d-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="32b0d-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="32b0d-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="32b0d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32b0d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b0d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32b0d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b0d-112">O caractere a ser exibido no lugar dos caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="32b0d-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="32b0d-113">Se esse parâmetro for zero, o controle removerá o caractere da senha atual e exibirá os caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="32b0d-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="32b0d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32b0d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b0d-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="32b0d-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b0d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32b0d-116">Return value</span></span>

<span data-ttu-id="32b0d-117">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="32b0d-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b0d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="32b0d-118">Remarks</span></span>

<span data-ttu-id="32b0d-119">Quando um controle de edição recebe a mensagem em **\_ SetPasswordChar** , o controle redesenha todos os caracteres visíveis usando o caractere especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="32b0d-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="32b0d-120">Se *wParam* for zero, o controle redesenhará todos os caracteres visíveis usando os caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="32b0d-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="32b0d-121">Se um controle de edição for criado com o estilo de [**\_ senha es**](edit-control-styles.md) , o caractere de senha padrão será definido como um asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="32b0d-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="32b0d-122">Se um controle de edição for criado sem o estilo de **\_ senha es** , não haverá nenhum caractere de senha.</span><span class="sxs-lookup"><span data-stu-id="32b0d-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="32b0d-123">O estilo **es \_ password** será removido se uma mensagem em **\_ SetPasswordChar** for enviada com o parâmetro *wParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="32b0d-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="32b0d-124">**Controles de edição:** Os controles de edição de várias linhas não dão suporte ao estilo de senha ou às mensagens.</span><span class="sxs-lookup"><span data-stu-id="32b0d-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="32b0d-125">**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="32b0d-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="32b0d-126">Os controles de linha única e de edição de várias linhas dão suporte ao estilo e às mensagens da senha.</span><span class="sxs-lookup"><span data-stu-id="32b0d-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="32b0d-127">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="32b0d-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32b0d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32b0d-128">Requirements</span></span>



| <span data-ttu-id="32b0d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="32b0d-129">Requirement</span></span> | <span data-ttu-id="32b0d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="32b0d-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b0d-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b0d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="32b0d-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32b0d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32b0d-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32b0d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="32b0d-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32b0d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32b0d-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32b0d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b0d-136"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32b0d-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b0d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="32b0d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b0d-138">**em \_ GETpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="32b0d-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 





