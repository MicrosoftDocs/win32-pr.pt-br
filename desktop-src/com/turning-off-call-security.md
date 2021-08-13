---
title: Como desligar a segurança de chamada
description: A segurança de chamada determina se um cliente tem permissão para chamar os métodos de um servidor. Há duas maneiras de desabilitar a segurança de chamada Uma envolve usar Dcomcnfg.exe modificar o registro e a outra requer chamadas para CoInitializeSecurity.
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
# <a name="turning-off-call-security"></a>Como desligar a segurança de chamada

A segurança de chamada determina se um cliente tem permissão para chamar os métodos de um servidor. Há duas maneiras de desabilitar a segurança de chamadas: uma envolve o uso de Dcomcnfg.exe para modificar o registro e a outra requer chamadas para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

-   [Desligar a segurança de chamada usando DCOMCNFG](#turning-off-call-security-using-dcomcnfg)
-   [Desligar a segurança de chamada programaticamente](#turning-off-call-security-programmatically)
-   [Tópicos relacionados](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>Desligar a segurança de chamada usando DCOMCNFG

A segurança de chamada pode ser desligada com mais facilidade usando Dcomcnfg.exe modificar o Registro. No entanto, Dcomcnfg.exe para desativar a segurança funcionará somente se o cliente e o servidor não [**chamarem CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Isso porque, quando **CoInitializeSecurity** é chamado, o DCOM ignora as configurações do Registro e usa os valores fornecidos para **CoInitializeSecurity.**

Para desativar a segurança com Dcomcnfg.exe, o cliente e o servidor devem definir seus Níveis de Autenticação como Nenhum. As etapas a seguir devem ser concluídas:

1.  Execute Dcomcnfg.exe.
2.  Na página **Aplicativos,** selecione o aplicativo que representa o servidor. Clique no **botão** Propriedades (ou clique duas vezes no aplicativo selecionado).
3.  Clique na guia **Geral**.
4.  Na caixa **de listagem Nível de** Autenticação Padrão, selecione **(Nenhum)**.
5.  Clique no **botão Aplicar** para aplicar alterações; no entanto, as alterações não são aplicadas a nenhuma instância em execução do aplicativo.
6.  Se o cliente aparecer na  lista na página Aplicativos, repita as etapas de 2 a 5, escolhendo o cliente em vez do servidor para a etapa 2. Em seguida, clique no botão **OK**. Se o cliente não estiver na lista, você poderá fazer uma das três seguintes coisas:
    -   Você pode definir o Nível de Autenticação do cliente como Nenhum em todo o computador usando Dcomcnfg.exe. (Consulte o aviso e o procedimento abaixo.)
    -   Você pode definir o nível de autenticação do cliente como Nenhum programaticamente.
    -   Você pode criar uma [chave AppID](appid-key.md) para o cliente para indicar um nível de autenticação Nenhum. (Consulte [Configurando Process-Wide segurança por meio do Registro](setting-processwide-security-through-the-registry.md).)

Para definir o Nível de Autenticação como Nenhum em todo o computador:

> [!Note]  
> Definir o nível de autenticação em todo o computador como Nenhum é extremamente não segura.

 

1.  Execute Dcomcnfg.exe.
2.  Escolha a **guia Propriedades** Padrão.
3.  Na caixa **de listagem Nível de** Autenticação Padrão, escolha **(Nenhum)**.
4.  Clique no botão **OK**.

## <a name="turning-off-call-security-programmatically"></a>Desligar a segurança de chamada programaticamente

Para desativar a segurança de chamada programaticamente, o cliente e o servidor devem chamar **CoInitializeSecurity**, definindo o nível de autenticação no parâmetro *dwAuthnLevel* como RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como desligar a segurança de ativação](turning-off-activation-security.md)
</dt> </dl>

 

 




