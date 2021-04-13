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
# <a name="managing-login"></a>Gerenciando o logon

O Windows Media Player dá suporte a uma variedade de métodos para que o usuário faça logon em uma loja do tipo 1 online. O Player fornece uma caixa de diálogo de logon padrão, mas a loja online pode fornecer uma página da Web que serve como uma alternativa à caixa de diálogo padrão.

O usuário pode iniciar uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta fornecida pela loja online. Se o usuário iniciar uma tentativa de logon interagindo com uma página de descoberta, o script na página de descoberta chamará o método [external. attemptLogin](external-attemptlogin.md) .

O estado de logon do usuário é mantido pela loja online. Quando o estado de logon do usuário for alterado, ou se uma tentativa de logon falhar, o plug-in do loja online notificará o Windows Media Player chamando [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange no parâmetro de *tipo* . O Player passa a notificação junto à página de descoberta, gerando o evento [external. OnLoginChange](external-onloginchange-event.md) .

Uma chamada para **OnLoginChange** não significa necessariamente que o estado de logon do usuário foi alterado; Isso pode significar que uma tentativa de fazer logon falhou. Para determinar o estado de logon do usuário, o manipulador de eventos **OnLoginChange** pode inspecionar a propriedade [external. userlogind](external-userloggedin.md) .

As seções a seguir descrevem o processo de logon padrão, o processo de logon alternativo e o processo de logout.

## <a name="standard-log-in"></a>Logon padrão

O processo de logon padrão envolve as seguintes etapas:

1.  O usuário inicia uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.
2.  O Windows Media Player exibe uma caixa de diálogo que solicita ao usuário um nome de usuário e uma senha.
3.  Quando o usuário clica no botão **entrar** na caixa de diálogo, o Windows Media Player chama [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), que é implementado pelo plug-in da loja online.
4.  O plug-in se comunica com a loja online e obtém êxito ou falha ao fazer logon no usuário.
5.  Se a tentativa de logon for realizada com sucesso, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ true no membro **boolVal** do parâmetro *pContext* . Se a tentativa de logon falhar, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando um valor de 32 bits no membro **UlVal** do parâmetro *pContext* . Em seguida, o Player passa esse valor de 32 bits para [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para obter a URL de uma página da Web que pode manipular a falha.

## <a name="alternative-login"></a>Logon alternativo

Se o \_ sinalizador ALTLOGIN do limite da assinatura \_ for definido na entrada do registro **Capabilities** para o plug-in da loja online, o Windows Media Player não usará a caixa de diálogo de logon padrão. Em vez disso, o Windows Media Player chama **IWMPContentPartner:: GetItemInfo** para recuperar a URL de uma página da Web que executa o processo de logon. Para obter mais informações sobre a entrada do registro **Capabilities** , consulte [chaves e entradas do registro para uma loja online tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

O jogador chama **GetItemInfo** duas vezes: uma vez passando g \_ szItemInfo \_ ALTLOGINURL para recuperar a URL da página da Web de logon e depois de passar g \_ szItemInfo \_ ALTLoginCaption para recuperar a legenda da janela que hospeda a página da Web. Quando **GetItemInfo** retorna a URL da página da Web de logon, ele pode especificar o tamanho da janela de logon acrescentando a seguinte cadeia de caracteres de parâmetro à URL:

? DlgX =*largura*&DlgY =*altura*

Na cadeia de caracteres do parâmetro, a *largura* e a *altura* são a largura e a altura da janela em pixels. Por exemplo, **GetItemInfo** poderia retornar a cadeia de caracteres a seguir para especificar que AltLogin.htm deve ser exibida em uma janela que tenha uma largura de 800 pixels e uma altura de 400 pixels


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



O processo de logon alternativo envolve as seguintes etapas:

1.  O usuário inicia uma tentativa de logon interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.
2.  O Windows Media Player abre uma janela modal que exibe a página da Web de logon fornecida pela loja online.
3.  A página da Web se comunica com a loja online e obtém êxito ou falha ao fazer logon no usuário.
4.  Se a tentativa de logon for realizada com sucesso, a página da Web notificará o plug-in da loja online chamando [external. SendMessage](external-sendmessage.md), o que resultará em uma chamada para [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). O plug-in do repositório online determina que a tentativa de logon foi bem-sucedida inspecionando os parâmetros passados para **IWMPContentPartner:: SendMessage**. Esses parâmetros não são interpretados pelo Windows Media Player; Eles têm significado apenas para a loja online. O plug-in chama **IWMPContentPartnerCallback:: Notify**, passando Variant \_ true no membro **boolVal** do parâmetro *pContext* . Se o logon falhar, o repositório online deverá determinar como auxiliar o usuário. Uma possibilidade é exibir uma nova página da Web na janela modal que hospeda a página da Web de logon alternativa.

## <a name="log-out"></a>Fazer logoff

O processo de logout envolve as etapas a seguir.

1.  O usuário inicia uma tentativa de logoff interagindo com a interface do usuário do Windows Media Player ou interagindo com uma página de descoberta.
2.  O Windows Media Player chama [IWMPContentPartner:: logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), que é implementado pelo plug-in da loja online.
3.  O plug-in se comunica com a loja online e obtém êxito ou falha ao fazer logoff do usuário.
4.  Se a tentativa de logout for realizada com sucesso, o plug-in notificará o Windows Media Player chamando **IWMPContentPartnerCallback:: Notify**, passando Variant \_ false no membro **boolVal** do parâmetro *pContext* .

Quando uma tentativa de fazer logon ou saída é bem-sucedida, o plug-in da loja online chama **IWMPContentPartnerCallback:: Notify**, passando wmpcnLoginStateChange no parâmetro de *tipo* . O plug-in usa o parâmetro *pContext* para especificar o estado de logon atual do usuário. Se o plug-in definir *pContext* -> **boolVal** como Variant \_ true, o usuário estará conectado. Se o plug-in definir *pContext* -> **boolVal** como Variant \_ false, o usuário será desconectado. Observe que o *pContext* não indica o êxito ou a falha da tentativa; em vez disso, indica o estado de logon atual do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento external. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userlogado**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: logon**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner:: logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




