---
title: Mensagem de WM_DDE_EXECUTE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de execução do WM \_ DDE \_ em um aplicativo de servidor DDE para enviar uma cadeia de caracteres ao servidor a ser processada como uma série de comandos.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Troca de dados de mensagem WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369679"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="b6dd1-104">Mensagem de execução de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="b6dd1-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="b6dd1-105">Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ execução do WM DDE** em um aplicativo de servidor DDE para enviar uma cadeia de caracteres ao servidor a ser processada como uma série de comandos.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="b6dd1-106">Espera-se que o aplicativo de servidor poste uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) em resposta.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="b6dd1-107">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="b6dd1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6dd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6dd1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6dd1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6dd1-110">Um identificador para a janela do cliente que está postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="b6dd1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6dd1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6dd1-112">Contém um objeto de memória global que faz referência a uma cadeia de caracteres de comando ANSI ou Unicode, dependendo dos tipos de janelas envolvidos na conversa.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6dd1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6dd1-113">Remarks</span></span>

<span data-ttu-id="b6dd1-114">A cadeia de caracteres de comando é uma cadeia de caracteres terminada em nulo que consiste em uma ou mais cadeias de código opcode entre colchetes simples ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="b6dd1-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="b6dd1-115">Cada cadeia de caracteres opcode tem a seguinte sintaxe, em que a lista de *parâmetros* é opcional:</span><span class="sxs-lookup"><span data-stu-id="b6dd1-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="b6dd1-116">*parâmetros de opcode*</span><span class="sxs-lookup"><span data-stu-id="b6dd1-116">*opcode parameters*</span></span>

<span data-ttu-id="b6dd1-117">O *opcode* é qualquer token único definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="b6dd1-118">Ele não pode incluir espaços, vírgulas, parênteses, colchetes ou aspas.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="b6dd1-119">A lista de *parâmetros* pode conter qualquer valor ou valores definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="b6dd1-120">Vários parâmetros são separados por vírgulas e a lista de parâmetros inteira é colocada entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="b6dd1-121">Os parâmetros não podem incluir vírgulas ou parênteses, exceto dentro de uma cadeia de caracteres entre aspas.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="b6dd1-122">Se um caractere de colchete ou parênteses for exibido em uma cadeia de caracteres entre aspas, ele não precisará ser duplicado, como foi o caso sob as regras antigas.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="b6dd1-123">Veja a seguir as cadeias de caracteres de comando válidas:</span><span class="sxs-lookup"><span data-stu-id="b6dd1-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="b6dd1-124">Observe que, sob as regras antigas, os parênteses e colchetes tinham que ser duplicados, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b6dd1-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="b6dd1-125">Os servidores devem ser capazes de analisar comandos em qualquer um dos formulários.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="b6dd1-126">As cadeias de caracteres de execução Unicode devem ser usadas somente quando os identificadores de janela do cliente e do servidor fazem com que a função [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="b6dd1-127">Lançamento</span><span class="sxs-lookup"><span data-stu-id="b6dd1-127">Posting</span></span>

<span data-ttu-id="b6dd1-128">O aplicativo cliente aloca o objeto de memória global chamando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="b6dd1-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="b6dd1-129">Ao processar a mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) que o servidor publica em resposta a uma mensagem de **\_ \_ execução de DDE do WM** , o aplicativo cliente deve excluir o objeto retornado pela mensagem de **\_ \_ confirmação DDE do WM** .</span><span class="sxs-lookup"><span data-stu-id="b6dd1-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="b6dd1-130">Recebimento</span><span class="sxs-lookup"><span data-stu-id="b6dd1-130">Receiving</span></span>

<span data-ttu-id="b6dd1-131">O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="b6dd1-132">O servidor deve reutilizar o objeto de memória global.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="b6dd1-133">A menos que especificado de outra forma por um subprotocolo, o servidor não deve postar a mensagem de [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) até que todas as ações especificadas pela cadeia de caracteres de comando execute sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="b6dd1-134">A única exceção a essa regra é quando a cadeia de caracteres faz com que o servidor encerre a conversa.</span><span class="sxs-lookup"><span data-stu-id="b6dd1-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6dd1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6dd1-135">Requirements</span></span>



| <span data-ttu-id="b6dd1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6dd1-136">Requirement</span></span> | <span data-ttu-id="b6dd1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b6dd1-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dd1-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6dd1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b6dd1-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6dd1-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b6dd1-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6dd1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b6dd1-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6dd1-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b6dd1-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b6dd1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6dd1-143"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6dd1-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dd1-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6dd1-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6dd1-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6dd1-146">**IsWindowUnicode**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="b6dd1-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="b6dd1-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="b6dd1-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="b6dd1-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="b6dd1-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="b6dd1-152">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="b6dd1-153">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b6dd1-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6dd1-154">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="b6dd1-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

