---
title: Mensagem de EM_LIMITTEXT (WinUser. h)
description: EM_LIMITTEXT mensagem – define o limite de texto de um controle de edição.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Controles de EM_LIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109784"
---
# <a name="em_limittext-message"></a><span data-ttu-id="ec2f1-104">\_Mensagem em LIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="ec2f1-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="ec2f1-105">Define o limite de texto de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="ec2f1-106">O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o usuário pode digitar no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="ec2f1-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="ec2f1-108">Para controles de edição e Microsoft Rich Edit 1,0, são usados bytes.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="ec2f1-109">Para o Microsoft rich edit 2,0 e posterior, são usados caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec2f1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec2f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2f1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec2f1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec2f1-112">O número máximo de **TCHAR** s que o usuário pode inserir.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="ec2f1-113">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="ec2f1-114">Esse número não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="ec2f1-115">**Controles de edição avançados:** Se esse parâmetro for zero, o tamanho do texto será definido como 64.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="ec2f1-116">Se esse parâmetro for zero, o tamanho do texto será definido como 0x7FFFFFFE caracteres para controles de edição de linha única ou-1 para controles de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f1-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec2f1-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec2f1-118">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2f1-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ec2f1-119">Return value</span></span>

<span data-ttu-id="ec2f1-120">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec2f1-121">Remarks</span></span>

<span data-ttu-id="ec2f1-122">A mensagem em **\_ LIMITTEXT** limita apenas o texto que o usuário pode inserir.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="ec2f1-123">Ele não afeta nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição pela mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="ec2f1-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="ec2f1-124">Se um aplicativo usar a **mensagem \_ SetText do WM** para posicionar mais texto em um controle de edição do que é especificado na mensagem em **\_ LIMITTEXT** , o usuário poderá editar todo o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="ec2f1-125">Antes **de \_ LIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir em um controle de edição é de 32.767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="ec2f1-126">Para controles de edição de linha única, o limite de texto é 0x7FFFFFFE bytes ou o valor do parâmetro *wParam* , o que for menor.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="ec2f1-127">Para controles de edição de várias linhas, esse valor é-1 byte ou o valor do parâmetro *wParam* , o que for menor.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="ec2f1-128">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ec2f1-129">Use a mensagem [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de comprimento de texto maiores que 64.000.</span><span class="sxs-lookup"><span data-stu-id="ec2f1-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="ec2f1-130">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ec2f1-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2f1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec2f1-131">Requirements</span></span>



| <span data-ttu-id="ec2f1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2f1-132">Requirement</span></span> | <span data-ttu-id="ec2f1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ec2f1-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f1-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec2f1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2f1-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec2f1-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec2f1-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec2f1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2f1-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec2f1-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec2f1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec2f1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec2f1-139"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f1-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec2f1-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ec2f1-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec2f1-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ec2f1-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ec2f1-142">**em \_ EXLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="ec2f1-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="ec2f1-143">**Editar \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="ec2f1-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="ec2f1-144">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="ec2f1-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ec2f1-145">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ec2f1-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

