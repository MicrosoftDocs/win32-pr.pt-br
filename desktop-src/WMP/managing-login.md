---
title: Gerenciando o logon
description: Gerenciando o logon
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Armazenamentos online do Windows Media Player, gerenciando logons
- lojas online, gerenciando logons
- Digite 1 lojas online, gerenciando logons
- Armazenamentos online do Windows Media Player, logons
- lojas online, logons
- Digite 1 lojas online, logons
- Armazenamentos online do Windows Media Player, processo de logon padrão
- lojas online, processo de logon padrão
- tipo 1 lojas online, processo de logon padrão
- Armazenamentos online do Windows Media Player, processo de logout
- lojas online, processo de logout
- tipo 1 lojas online, processo de logout
- processo de logon padrão
- processo de logout
- logons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365579"
---
# <a name="managing-login"></a><span data-ttu-id="09a31-118">Gerenciando o logon</span><span class="sxs-lookup"><span data-stu-id="09a31-118">Managing Login</span></span>

<span data-ttu-id="09a31-119">O Windows Media Player dá suporte a uma variedade de métodos para que o usuário faça logon em uma loja do tipo 1 online.</span><span class="sxs-lookup"><span data-stu-id="09a31-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="09a31-120">O Player fornece uma caixa de diálogo de logon padrão, mas a loja online pode fornecer uma página da Web que serve como uma alternativa à caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="09a31-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="09a31-121">O usuário pode iniciar uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta fornecida pela loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="09a31-122">Se o usuário iniciar uma tentativa de logon interagindo com uma página de descoberta, o script na página de descoberta chamará o método [external. attemptLogin](external-attemptlogin.md) .</span><span class="sxs-lookup"><span data-stu-id="09a31-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="09a31-123">O estado de logon do usuário é mantido pela loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="09a31-124">Quando o estado de logon do usuário for alterado, ou se uma tentativa de logon falhar, o plug-in do loja online notificará o Windows Media Player chamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange no parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="09a31-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="09a31-125">O Player passa a notificação junto à página de descoberta, gerando o evento [external. OnLoginChange](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="09a31-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="09a31-126">Uma chamada para **OnLoginChange** não significa necessariamente que o estado de logon do usuário foi alterado; Isso pode significar que uma tentativa de fazer logon falhou.</span><span class="sxs-lookup"><span data-stu-id="09a31-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="09a31-127">Para determinar o estado de logon do usuário, o manipulador de eventos **OnLoginChange** pode inspecionar a propriedade [external. userlogind](external-userloggedin.md) .</span><span class="sxs-lookup"><span data-stu-id="09a31-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="09a31-128">As seções a seguir descrevem o processo de logon padrão, o processo de logon alternativo e o processo de logout.</span><span class="sxs-lookup"><span data-stu-id="09a31-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="09a31-129">Logon padrão</span><span class="sxs-lookup"><span data-stu-id="09a31-129">Standard Log-in</span></span>

<span data-ttu-id="09a31-130">O processo de logon padrão envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="09a31-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="09a31-131">O usuário inicia uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="09a31-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="09a31-132">O Windows Media Player exibe uma caixa de diálogo que solicita ao usuário um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="09a31-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="09a31-133">Quando o usuário clica no botão **entrar** na caixa de diálogo, o Windows Media Player chama [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), que é implementado pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="09a31-134">O plug-in se comunica com a loja online e obtém êxito ou falha ao fazer logon no usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="09a31-135">Se a tentativa de logon for realizada com sucesso, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ true no membro **boolVal** do parâmetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="09a31-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="09a31-136">Se a tentativa de logon falhar, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando um valor de 32 bits no membro **UlVal** do parâmetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="09a31-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="09a31-137">Em seguida, o Player passa esse valor de 32 bits para [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para obter a URL de uma página da Web que pode manipular a falha.</span><span class="sxs-lookup"><span data-stu-id="09a31-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="09a31-138">Logon alternativo</span><span class="sxs-lookup"><span data-stu-id="09a31-138">Alternative Login</span></span>

<span data-ttu-id="09a31-139">Se o \_ sinalizador ALTLOGIN do limite da assinatura \_ for definido na entrada do registro **Capabilities** para o plug-in da loja online, o Windows Media Player não usará a caixa de diálogo de logon padrão.</span><span class="sxs-lookup"><span data-stu-id="09a31-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="09a31-140">Em vez disso, o Windows Media Player chama **IWMPContentPartner:: GetItemInfo** para recuperar a URL de uma página da Web que executa o processo de logon.</span><span class="sxs-lookup"><span data-stu-id="09a31-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="09a31-141">Para obter mais informações sobre a entrada do registro **Capabilities** , consulte [chaves e entradas do registro para uma loja online tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="09a31-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="09a31-142">O jogador chama **GetItemInfo** duas vezes: uma vez passando g \_ szItemInfo \_ ALTLOGINURL para recuperar a URL da página da Web de logon e depois de passar g \_ szItemInfo \_ ALTLoginCaption para recuperar a legenda da janela que hospeda a página da Web.</span><span class="sxs-lookup"><span data-stu-id="09a31-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="09a31-143">Quando **GetItemInfo** retorna a URL da página da Web de logon, ele pode especificar o tamanho da janela de logon acrescentando a seguinte cadeia de caracteres de parâmetro à URL:</span><span class="sxs-lookup"><span data-stu-id="09a31-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="09a31-144">? DlgX =*largura*&DlgY =*altura*</span><span class="sxs-lookup"><span data-stu-id="09a31-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="09a31-145">Na cadeia de caracteres do parâmetro, a *largura* e a *altura* são a largura e a altura da janela em pixels.</span><span class="sxs-lookup"><span data-stu-id="09a31-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="09a31-146">Por exemplo, **GetItemInfo** poderia retornar a cadeia de caracteres a seguir para especificar que AltLogin.htm deve ser exibida em uma janela que tenha uma largura de 800 pixels e uma altura de 400 pixels</span><span class="sxs-lookup"><span data-stu-id="09a31-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="09a31-147">O processo de logon alternativo envolve as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="09a31-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="09a31-148">O usuário inicia uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="09a31-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="09a31-149">O Windows Media Player abre uma janela modal que exibe a página da Web de logon fornecida pela loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="09a31-150">A página da Web se comunica com a loja online e obtém êxito ou falha ao fazer logon no usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="09a31-151">Se a tentativa de logon for realizada com sucesso, a página da Web notificará o plug-in da loja online chamando [external. SendMessage](external-sendmessage.md), o que resultará em uma chamada para [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="09a31-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="09a31-152">O plug-in do repositório online determina que a tentativa de logon foi bem-sucedida inspecionando os parâmetros passados para **IWMPContentPartner:: SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="09a31-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="09a31-153">Esses parâmetros não são interpretados pelo Windows Media Player; Eles têm significado apenas para a loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="09a31-154">O plug-in chama **IWMPContentPartnerCallback:: Notify**, passando Variant \_ true no membro **boolVal** do parâmetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="09a31-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="09a31-155">Se o logon falhar, o repositório online deverá determinar como auxiliar o usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="09a31-156">Uma possibilidade é exibir uma nova página da Web na janela modal que hospeda a página da Web de logon alternativa.</span><span class="sxs-lookup"><span data-stu-id="09a31-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="09a31-157">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="09a31-157">Log-out</span></span>

<span data-ttu-id="09a31-158">O processo de logout envolve as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="09a31-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="09a31-159">O usuário inicia uma tentativa de logoff interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="09a31-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="09a31-160">O Windows Media Player chama [IWMPContentPartner:: logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), que é implementado pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="09a31-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="09a31-161">O plug-in se comunica com a loja online e obtém êxito ou falha ao fazer logoff do usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="09a31-162">Se a tentativa de logout for realizada com sucesso, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ false no membro **boolVal** do parâmetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="09a31-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="09a31-163">Quando uma tentativa de fazer logon ou saída é bem-sucedida, o plug-in da loja online chama **IWMPContentPartnerCallback:: Notify**, passando wmpcnLoginStateChange no parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="09a31-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="09a31-164">O plug-in usa o parâmetro *pContext* para especificar o estado de logon atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="09a31-165">Se o plug-in definir *pContext* -> **boolVal** como Variant \_ true, o usuário estará conectado.</span><span class="sxs-lookup"><span data-stu-id="09a31-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="09a31-166">Se o plug-in definir *pContext* -> **boolVal** como Variant \_ false, o usuário será desconectado. Observe que o *pContext* não indica o êxito ou a falha da tentativa; em vez disso, indica o estado de logon atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="09a31-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09a31-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09a31-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a31-168">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="09a31-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="09a31-169">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="09a31-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="09a31-170">**External. userlogado**</span><span class="sxs-lookup"><span data-stu-id="09a31-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="09a31-171">**IWMPContentPartner:: logon**</span><span class="sxs-lookup"><span data-stu-id="09a31-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="09a31-172">**IWMPContentPartner:: logout**</span><span class="sxs-lookup"><span data-stu-id="09a31-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="09a31-173">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="09a31-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




