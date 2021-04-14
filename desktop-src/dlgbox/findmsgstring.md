---
title: Mensagem de FINDMSGSTRING (Commdlg. h)
description: Uma caixa de diálogo Localizar ou substituir envia a mensagem registrada FINDMSGSTRING para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão Localizar próximo, substituir ou substituir tudo ou fecha a caixa de diálogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Caixas de diálogo de mensagem FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499740"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="99444-104">Mensagem FINDMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="99444-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="99444-105">Uma caixa de diálogo **Localizar** ou **substituir** envia a mensagem registrada **FINDMSGSTRING** para o procedimento de janela de sua janela do proprietário quando o usuário clica no botão **Localizar próximo**, **substituir** ou **substituir tudo** ou fecha a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="99444-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="99444-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99444-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99444-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99444-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="99444-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="99444-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99444-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99444-110">Um ponteiro para uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .</span><span class="sxs-lookup"><span data-stu-id="99444-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="99444-111">Os membros dessa estrutura contêm a entrada de usuário mais recente, incluindo a cadeia de caracteres a ser pesquisada, a cadeia de caracteres de substituição (se houver) e as opções de pesquisa e substituição.</span><span class="sxs-lookup"><span data-stu-id="99444-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99444-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99444-112">Return value</span></span>

<span data-ttu-id="99444-113">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="99444-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99444-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="99444-114">Remarks</span></span>

<span data-ttu-id="99444-115">Você deve especificar a constante **FINDMSGSTRING** em uma chamada para a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter o identificador para a mensagem enviada pela caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="99444-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="99444-116">Ao criar a caixa de diálogo, use o membro **hwndOwner** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para identificar a janela para receber mensagens **FINDMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="99444-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="99444-117">O membro **flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) inclui um dos sinalizadores a seguir para indicar o evento que causou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="99444-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="99444-118">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="99444-118">Flag</span></span>                            | <span data-ttu-id="99444-119">Significado</span><span class="sxs-lookup"><span data-stu-id="99444-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99444-120">**Fr \_ DIALOGTERM** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="99444-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="99444-121">A caixa de diálogo está fechando.</span><span class="sxs-lookup"><span data-stu-id="99444-121">The dialog box is closing.</span></span> <span data-ttu-id="99444-122">Depois que a janela do proprietário processa essa mensagem, um identificador para a caixa de diálogo não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="99444-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="99444-123">**Fr \_ LOCALIZARPRÓXIMO** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="99444-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="99444-124">O usuário clicou no botão **Localizar próximo** em uma caixa de diálogo **Localizar** ou **substituir** .</span><span class="sxs-lookup"><span data-stu-id="99444-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="99444-125">O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="99444-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="99444-126">**Fr \_ REPLACE** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="99444-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="99444-127">O usuário clicou no botão **substituir** em uma caixa de diálogo **substituir** .</span><span class="sxs-lookup"><span data-stu-id="99444-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="99444-128">O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição.</span><span class="sxs-lookup"><span data-stu-id="99444-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="99444-129">**Fr \_ REPLACEALL** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="99444-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="99444-130">O usuário clicou no botão **substituir tudo** em uma caixa de diálogo **substituir** .</span><span class="sxs-lookup"><span data-stu-id="99444-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="99444-131">O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição.</span><span class="sxs-lookup"><span data-stu-id="99444-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="99444-132">Para uma mensagem **Localizar próximo** ou **substituir tudo** , o membro **sinalizadores** pode incluir um ou mais dos sinalizadores a seguir para indicar as opções de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="99444-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="99444-133">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="99444-133">Flag</span></span>                           | <span data-ttu-id="99444-134">Significado</span><span class="sxs-lookup"><span data-stu-id="99444-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99444-135">**Fr \_ INOPERANTE** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="99444-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="99444-136">Se definido, o botão **para baixo** da direção botões de opção é selecionado indicando que o usuário deseja pesquisar do local atual até o fim do documento.</span><span class="sxs-lookup"><span data-stu-id="99444-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="99444-137">Se **fr \_ baixo** não estiver definido, o botão para **cima** será selecionado para que o usuário queira Pesquisar até o início do documento.</span><span class="sxs-lookup"><span data-stu-id="99444-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="99444-138">**Fr \_ MATCHCASE** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="99444-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="99444-139">Se definido, a caixa de seleção **diferenciar maiúsculas de minúsculas** é marcada indicando que o usuário quer que a pesquisa diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="99444-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="99444-140">Se **fr \_ MATCHCASE** não estiver definido, a caixa de seleção será desmarcada, de modo que a pesquisa não deve diferenciar maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="99444-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="99444-141">**Fr \_ WHOLEWORD** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="99444-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="99444-142">Se definido, a caixa de seleção **corresponder somente palavra inteira** estará marcada indicando que o usuário deseja pesquisar apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="99444-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="99444-143">Se **fr \_ WHOLEWORD** não for definido, a caixa de seleção será desmarcada, de modo que você também deverá Pesquisar fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="99444-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="99444-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99444-144">Requirements</span></span>



| <span data-ttu-id="99444-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="99444-145">Requirement</span></span> | <span data-ttu-id="99444-146">Valor</span><span class="sxs-lookup"><span data-stu-id="99444-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99444-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99444-147">Minimum supported client</span></span><br/> | <span data-ttu-id="99444-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99444-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99444-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99444-149">Minimum supported server</span></span><br/> | <span data-ttu-id="99444-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99444-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99444-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99444-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="99444-152"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99444-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="99444-153">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="99444-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="99444-154">**FINDMSGSTRINGW** (Unicode) e **FINDMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="99444-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="99444-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="99444-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="99444-156">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99444-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99444-157">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="99444-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="99444-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="99444-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="99444-159">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="99444-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99444-160">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="99444-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

