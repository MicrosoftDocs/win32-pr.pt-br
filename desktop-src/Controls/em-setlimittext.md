---
title: Mensagem de EM_SETLIMITTEXT (WinUser. h)
description: Define o limite de texto de um controle de edição.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Controles de EM_SETLIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644776"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="8cfa0-104">\_Mensagem em SETLIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="8cfa0-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="8cfa0-105">Define o limite de texto de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="8cfa0-106">O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o usuário pode digitar no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="8cfa0-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="8cfa0-108">Para controles de edição e Microsoft Rich Edit 1,0, são usados bytes.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="8cfa0-109">Para o Microsoft rich edit 2,0 e posterior, são usados caracteres.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="8cfa0-110">A mensagem em **\_ SETLIMITTEXT** é idêntica à mensagem [**em \_ LIMITTEXT**](em-limittext.md) .</span><span class="sxs-lookup"><span data-stu-id="8cfa0-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cfa0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cfa0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfa0-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cfa0-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cfa0-113">O número máximo de **TCHAR** s que o usuário pode inserir.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="8cfa0-114">Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="8cfa0-115">Esse número não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="8cfa0-116">**Controles de edição avançados:** Se esse parâmetro for zero, o tamanho do texto será definido como 64.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="8cfa0-117">Se esse parâmetro for zero, o tamanho do texto será definido como 0x7FFFFFFE caracteres para controles de edição de linha única ou 1 para controles de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="8cfa0-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cfa0-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cfa0-119">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfa0-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cfa0-120">Return value</span></span>

<span data-ttu-id="8cfa0-121">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cfa0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cfa0-122">Remarks</span></span>

<span data-ttu-id="8cfa0-123">A mensagem em **\_ SETLIMITTEXT** limita apenas o texto que o usuário pode inserir.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="8cfa0-124">Ele não afeta nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição pela mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="8cfa0-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="8cfa0-125">Se um aplicativo usar a **mensagem \_ SetText do WM** para posicionar mais texto em um controle de edição do que é especificado na mensagem em **\_ SETLIMITTEXT** , o usuário poderá editar todo o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="8cfa0-126">Antes **de \_ SETLIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir em um controle de edição é de 32.767 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="8cfa0-127">Para controles de edição de linha única, o limite de texto é 0x7FFFFFFE bytes ou o valor do parâmetro *wParam* , o que for menor.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="8cfa0-128">Para controles de edição de várias linhas, esse valor é 1 bytes ou o valor do parâmetro *wParam* , o que for menor.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="8cfa0-129">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8cfa0-130">Use a mensagem [**em \_ EXLIMITTEXT**](em-exlimittext.md) para valores de comprimento de texto maiores que 64.000.</span><span class="sxs-lookup"><span data-stu-id="8cfa0-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="8cfa0-131">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8cfa0-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfa0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cfa0-132">Requirements</span></span>



| <span data-ttu-id="8cfa0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cfa0-133">Requirement</span></span> | <span data-ttu-id="8cfa0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfa0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfa0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cfa0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8cfa0-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cfa0-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8cfa0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cfa0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8cfa0-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cfa0-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8cfa0-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cfa0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cfa0-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cfa0-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cfa0-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8cfa0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfa0-142">**em \_ GETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="8cfa0-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

