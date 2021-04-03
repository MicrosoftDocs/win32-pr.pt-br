---
title: Considerações sobre segurança controles do Microsoft Windows
description: Este tópico fornece informações sobre considerações de segurança relacionadas aos controles do Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084973"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="8549e-103">Considerações de segurança: controles do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="8549e-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="8549e-104">Este tópico fornece informações sobre considerações de segurança relacionadas aos controles do Windows.</span><span class="sxs-lookup"><span data-stu-id="8549e-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="8549e-105">As informações neste tópico não fornecem tudo o que você precisa saber sobre problemas de segurança — Use-o como ponto de partida e referência para essa área de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="8549e-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="8549e-106">A interconectividade entre computadores é comum; a principal preocupação do desenvolvedor deve ser a segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8549e-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="8549e-107">As seções a seguir discutem alguns possíveis problemas de segurança a serem considerados ao programar controles do Windows.</span><span class="sxs-lookup"><span data-stu-id="8549e-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="8549e-108">Mensagens de controle terminadas em nulo</span><span class="sxs-lookup"><span data-stu-id="8549e-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="8549e-109">Uso de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8549e-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="8549e-110">Validação da entrada</span><span class="sxs-lookup"><span data-stu-id="8549e-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="8549e-111">Uso de senha</span><span class="sxs-lookup"><span data-stu-id="8549e-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="8549e-112">Alertas de segurança</span><span class="sxs-lookup"><span data-stu-id="8549e-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="8549e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8549e-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="8549e-114">Mensagens de controle terminadas em nulo</span><span class="sxs-lookup"><span data-stu-id="8549e-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="8549e-115">Muitas das mensagens de controle e macros têm parâmetros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="8549e-116">Geralmente, essas mensagens não validam as cadeias de caracteres de entrada, em particular, não verificam se há um encerramento `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="8549e-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="8549e-117">Quando você chama uma mensagem que usa uma cadeia de caracteres como parâmetro, especifique explicitamente que a cadeia de caracteres é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="8549e-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="8549e-118">Uso de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8549e-118">String Use</span></span>

<span data-ttu-id="8549e-119">Quando você programa os controles do Windows, é necessário manipular cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="8549e-120">Quase todos os controles exigem que o texto seja inserido.</span><span class="sxs-lookup"><span data-stu-id="8549e-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="8549e-121">Por exemplo, para preencher uma caixa de listagem, você deve carregar cadeias de caracteres no controle.</span><span class="sxs-lookup"><span data-stu-id="8549e-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="8549e-122">Como usar cadeias de caracteres incorretamente geralmente causa estouros de buffer, tome precauções para evitar esse risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="8549e-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="8549e-123">Para obter mais informações sobre estouros de buffer, consulte *escrevendo código seguro* por Michael Howard e David LeBlanc, Microsoft Press, 2002 e práticas [recomendadas para as APIs de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="8549e-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="8549e-124">Validação da entrada</span><span class="sxs-lookup"><span data-stu-id="8549e-124">Input Validation</span></span>

<span data-ttu-id="8549e-125">As mensagens de controle a seguir podem apresentar problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="8549e-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="8549e-126">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="8549e-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="8549e-127">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="8549e-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="8549e-128">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="8549e-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="8549e-129">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="8549e-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="8549e-130">**TB de \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="8549e-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="8549e-131">**TTM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="8549e-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="8549e-132">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="8549e-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="8549e-133">Se o texto for alterado entre a chamada para obter o comprimento do texto e a hora em que o texto for exibido ou usado, poderá ocorrer uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="8549e-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="8549e-134">Para evitar isso, você deve validar a cadeia de caracteres antes de usá-la.</span><span class="sxs-lookup"><span data-stu-id="8549e-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="8549e-135">Além disso, as mensagens que recuperam texto, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)e [**TTM \_ gettext**](ttm-gettext.md), não têm nenhum parâmetro de tamanho de buffer que apresente o potencial para uma saturação de buffer.</span><span class="sxs-lookup"><span data-stu-id="8549e-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="8549e-136">Ao usar [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou [**SB \_ gettext**](sb-gettext.md), você deve primeiro chamar [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) ou [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="8549e-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="8549e-137">Algumas dessas mensagens, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)e [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), podem ser chamadas com um valor de parâmetro **nulo** para obter o comprimento da cadeia de caracteres antes de invocar a mensagem para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="8549e-138">Uma mensagem que você deve prestar atenção especial é a mensagem da barra de status [**SB \_ GETTIPTEXT**](sb-gettiptext.md) .</span><span class="sxs-lookup"><span data-stu-id="8549e-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="8549e-139">Essa mensagem não fornece nenhuma maneira de consultar o comprimento da cadeia de caracteres que será recuperada.</span><span class="sxs-lookup"><span data-stu-id="8549e-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="8549e-140">Uso de senha</span><span class="sxs-lookup"><span data-stu-id="8549e-140">Password Use</span></span>

<span data-ttu-id="8549e-141">Se você usar controles de edição protegidos por senha (estilo de [**\_ senha es**](edit-control-styles.md) ), o buffer que contém o texto recuperado deverá ser definido como zero assim que possível para evitar a exposição da senha do usuário na memória.</span><span class="sxs-lookup"><span data-stu-id="8549e-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="8549e-142">Alertas de segurança</span><span class="sxs-lookup"><span data-stu-id="8549e-142">Security Alerts</span></span>

<span data-ttu-id="8549e-143">A tabela a seguir lista os recursos que, se usados incorretamente, podem comprometer a segurança de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8549e-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="8549e-144">As mensagens listadas aqui não fornecem um parâmetro que especifica o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="8549e-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="8549e-145">Recurso</span><span class="sxs-lookup"><span data-stu-id="8549e-145">Feature</span></span>                                               | <span data-ttu-id="8549e-146">Atenuação</span><span class="sxs-lookup"><span data-stu-id="8549e-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8549e-147">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="8549e-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="8549e-148">Verifique se o buffer usado pela função pode ser gravado e se está terminando em nulo.</span><span class="sxs-lookup"><span data-stu-id="8549e-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="8549e-149">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="8549e-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="8549e-150">Chame [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obter o tamanho do buffer e, em seguida, chame [**CB \_ GETLBTEXT**](cb-getlbtext.md) para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="8549e-151">**\_GETISEARCHSTRING LVM**</span><span class="sxs-lookup"><span data-stu-id="8549e-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="8549e-152">Chame a mensagem com um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="8549e-153">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="8549e-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="8549e-154">Chame [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o tamanho do buffer e, em seguida, chame [**SB \_ gettext**](sb-gettext.md) para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="8549e-155">**TB de \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="8549e-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="8549e-156">Chame a mensagem com um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="8549e-157">**TTM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="8549e-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="8549e-158">Essa mensagem não fornece uma maneira de saber ou especificar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="8549e-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="8549e-159">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="8549e-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="8549e-160">Chame a mensagem passando um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8549e-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="8549e-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8549e-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8549e-162">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8549e-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8549e-163">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="8549e-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="8549e-164">Segurança</span><span class="sxs-lookup"><span data-stu-id="8549e-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="8549e-165">Recursos de segurança do TechNet</span><span class="sxs-lookup"><span data-stu-id="8549e-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="8549e-166">Práticas recomendadas para as APIs de segurança</span><span class="sxs-lookup"><span data-stu-id="8549e-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 