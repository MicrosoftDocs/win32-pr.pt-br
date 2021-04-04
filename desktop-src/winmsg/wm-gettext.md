---
description: Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Mensagem de WM_GETTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662596"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="c55e4-103">\_Mensagem de GETtext do WM</span><span class="sxs-lookup"><span data-stu-id="c55e4-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="c55e4-104">Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="c55e4-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="c55e4-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c55e4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55e4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c55e4-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c55e4-107">O número máximo de caracteres a serem copiados, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c55e4-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="c55e4-108">Os aplicativos ANSI podem ter a cadeia de caracteres no buffer reduzida em tamanho (até um mínimo de metade do valor *wParam* ) devido à conversão de ANSI para Unicode.</span><span class="sxs-lookup"><span data-stu-id="c55e4-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="c55e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c55e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c55e4-110">Um ponteiro para o buffer que deve receber o texto.</span><span class="sxs-lookup"><span data-stu-id="c55e4-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55e4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c55e4-111">Return value</span></span>

<span data-ttu-id="c55e4-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c55e4-112">Type: **LRESULT**</span></span>

<span data-ttu-id="c55e4-113">O valor de retorno é o número de caracteres copiados, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c55e4-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="c55e4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c55e4-114">Remarks</span></span>

<span data-ttu-id="c55e4-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia o texto associado à janela no buffer especificado e retorna o número de caracteres copiados.</span><span class="sxs-lookup"><span data-stu-id="c55e4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="c55e4-116">Observe que, para controles estáticos que não são de texto, isso lhe dá o texto com o qual o controle foi originalmente criado, ou seja, o número de ID.</span><span class="sxs-lookup"><span data-stu-id="c55e4-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="c55e4-117">No entanto, ele fornece a ID do controle estático de não texto como criado originalmente.</span><span class="sxs-lookup"><span data-stu-id="c55e4-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="c55e4-118">Ou seja, se você usou subseqüentemente um **STM \_ SetImage** para alterá-lo, a ID original ainda seria retornada.</span><span class="sxs-lookup"><span data-stu-id="c55e4-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="c55e4-119">Para um controle de edição, o texto a ser copiado é o conteúdo do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="c55e4-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="c55e4-120">Para uma caixa de combinação, o texto é o conteúdo da parte do controle de edição (ou texto estático) da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="c55e4-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="c55e4-121">Para um botão, o texto é o nome do botão.</span><span class="sxs-lookup"><span data-stu-id="c55e4-121">For a button, the text is the button name.</span></span> <span data-ttu-id="c55e4-122">Para outras janelas, o texto é o título da janela.</span><span class="sxs-lookup"><span data-stu-id="c55e4-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="c55e4-123">Para copiar o texto de um item em uma caixa de listagem, um aplicativo pode usar a mensagem [**\_ gettext do lb**](../controls/lb-gettext.md) .</span><span class="sxs-lookup"><span data-stu-id="c55e4-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="c55e4-124">Quando a mensagem do **WM \_ gettext** é enviada a um controle estático com o estilo de **\_ ícone SS** , um identificador para o ícone será retornado nos primeiros quatro bytes do buffer apontado por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c55e4-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="c55e4-125">Isso será verdadeiro somente se a [**mensagem \_ SetText do WM**](wm-settext.md) tiver sido usada para definir o ícone.</span><span class="sxs-lookup"><span data-stu-id="c55e4-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="c55e4-126">**Edição avançada:** Se o texto a ser copiado exceder 64K, use a mensagem em [**\_ StreamOut**](../controls/em-streamout.md) ou em [**\_ GETSELTEXT**](../controls/em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="c55e4-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="c55e4-127">Enviar uma mensagem de **\_ gettext do WM** para um controle estático de não texto, como um bitmap estático ou um controle de ícone estático, não retorna um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c55e4-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="c55e4-128">Em vez disso, retorna zero.</span><span class="sxs-lookup"><span data-stu-id="c55e4-128">Instead, it returns zero.</span></span> <span data-ttu-id="c55e4-129">Além disso, nas versões anteriores do Windows, os aplicativos podiam enviar uma mensagem de **\_ gettext do WM** a um controle estático não texto para recuperar a ID do controle.</span><span class="sxs-lookup"><span data-stu-id="c55e4-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="c55e4-130">Para recuperar a ID de um controle, os aplicativos podem usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando a **\_ ID GWL** como o valor de índice ou [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando a **\_ ID de GWLP**.</span><span class="sxs-lookup"><span data-stu-id="c55e4-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55e4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c55e4-131">Requirements</span></span>



| <span data-ttu-id="c55e4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c55e4-132">Requirement</span></span> | <span data-ttu-id="c55e4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c55e4-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55e4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c55e4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c55e4-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c55e4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c55e4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c55e4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c55e4-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c55e4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c55e4-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c55e4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c55e4-139"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c55e4-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55e4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c55e4-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="c55e4-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c55e4-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c55e4-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c55e4-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c55e4-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="c55e4-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="c55e4-144">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="c55e4-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="c55e4-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="c55e4-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="c55e4-146">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="c55e4-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="c55e4-147">**GETTEXTLENGTH do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c55e4-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="c55e4-148">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c55e4-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="c55e4-149">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c55e4-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c55e4-150">Windows</span><span class="sxs-lookup"><span data-stu-id="c55e4-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="c55e4-151">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c55e4-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c55e4-152">**em \_ GETSELTEXT**</span><span class="sxs-lookup"><span data-stu-id="c55e4-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="c55e4-153">**em \_ fluxo contínuo**</span><span class="sxs-lookup"><span data-stu-id="c55e4-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="c55e4-154">**LB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="c55e4-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
