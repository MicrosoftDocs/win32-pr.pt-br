---
title: Desativando a segurança da chamada
description: A chamada de segurança determina se um cliente tem permissão para chamar os métodos de um servidor. Há duas maneiras de desabilitar a segurança de chamada um envolve o uso de Dcomcnfg.exe para modificar o registro e o outro requer chamadas para CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d8d8f4a48baed00655761e89a12f0aa84846a0a2defdc0b2e444b2bee9103f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550560"
---
# <a name="turning-off-call-security"></a>Desativando a segurança da chamada

A chamada de segurança determina se um cliente tem permissão para chamar os métodos de um servidor. Há duas maneiras de desabilitar a segurança da chamada: uma envolve o uso de Dcomcnfg.exe para modificar o registro e o outro requer chamadas para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Desligando a segurança da chamada usando DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Desligando a segurança da chamada de forma programática](#turning-off-call-security-programmatically)
-   [Tópicos relacionados](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Desligando a segurança da chamada usando DCOMCNFG

A segurança da chamada pode ser desativada com mais facilidade usando Dcomcnfg.exe para modificar o registro. No entanto, o uso de Dcomcnfg.exe para desativar a segurança só funcionará se o cliente e o servidor não chamarem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Isso ocorre porque quando **CoInitializeSecurity** é chamado, o DCOM ignora as configurações do registro e usa os valores fornecidos para **CoInitializeSecurity** em vez disso.

Para desativar a segurança com Dcomcnfg.exe, o cliente e o servidor devem definir seus níveis de autenticação como nenhum. As etapas a seguir devem ser concluídas:

1.  Execute Dcomcnfg.exe.
2.  Na página **aplicativos** , selecione o aplicativo que representa o servidor. Clique no botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).
3.  Clique na guia **Geral**.
4.  Na caixa de listagem **nível de autenticação padrão** , selecione **(nenhum)**.
5.  Clique no botão **aplicar** para aplicar as alterações; no entanto, as alterações não são aplicadas a nenhuma instância em execução do aplicativo.
6.  Se o cliente aparecer na lista na página *aplicativos* , repita as etapas de 2 a 5, escolhendo o cliente em vez do servidor para a etapa 2. Em seguida, clique no botão **OK**. Se o cliente não estiver na lista, você poderá executar uma das três ações a seguir:
    -   Você pode definir o nível de autenticação do cliente como nenhum em todo o computador usando Dcomcnfg.exe. (Consulte o aviso e o procedimento abaixo.)
    -   Você pode definir o nível de autenticação do cliente como nenhum programaticamente.
    -   Você pode criar uma chave [AppID](appid-key.md) para o cliente para indicar um nível de autenticação de nenhum. (Consulte [definir Process-Wide segurança por meio do registro](setting-processwide-security-through-the-registry.md).)

Para definir o nível de autenticação como None em todo o computador:

> [!Note]  
> Definir o nível de autenticação em todo o computador como nenhum é extremamente inseguro.

 

1.  Execute Dcomcnfg.exe.
2.  Escolha a guia **propriedades padrão** .
3.  Na caixa de listagem **nível de autenticação padrão** , escolha **(nenhum)**.
4.  Clique no botão **OK**.

## <a name="turning-off-call-security-programmatically"></a>Desligando a segurança da chamada de forma programática

Para desativar a segurança de chamada por meio de programação, o cliente e o servidor devem chamar **CoInitializeSecurity**, definindo o nível de autenticação no parâmetro *dwAuthnLevel* como RPC \_ C \_ Authn \_ nível \_ None.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desativando a segurança de ativação](turning-off-activation-security.md)
</dt> </dl>

 

 




