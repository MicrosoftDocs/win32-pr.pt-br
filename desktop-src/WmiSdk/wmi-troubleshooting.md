---
description: Ao acessar dados locais ou remotos do WMI em um aplicativo ou script, você pode encontrar erros que variam de classes ausentes a acesso negado. Os provedores também têm opções de depuração e de solução de problemas disponíveis.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Solução de problemas do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40645c33da838658d66f608d672d979b38012fa855f26637f5896c4ec14c54ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794286"
---
# <a name="wmi-troubleshooting"></a>Solução de problemas do WMI

Ao acessar dados locais ou remotos do WMI em um aplicativo ou script, você pode encontrar erros que variam de classes ausentes a acesso negado. Os provedores também têm opções de depuração e de solução de problemas disponíveis.

> [!Note]  
> A documentação a seguir destina-se a desenvolvedores e administradores de ti. Se você for um usuário final que recebeu uma mensagem de erro relacionada ao WMI, vá para [suporte da Microsoft](https://support.microsoft.com/) e procure o código de erro que você vê na mensagem de erro. Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte o [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilitário de Diagnóstico WMI

o utilitário de diagnóstico WMI (WMIDiag.exe) não tem mais suporte a partir de Windows 8 e Windows Server 2012.

* * Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008: * *

Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.

para obter mais informações sobre a origem do problema, você pode baixar e executar a ferramenta de linha de comando de diagnóstico [Utilitário de Diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo. você pode baixar o Utilitário de Diagnóstico WMI no [centro de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

Os gravadores de provedor também podem encontrar problemas de depuração, a menos que você esteja escrevendo um [*provedor dissociado*](gloss-d.md). Para obter mais informações, consulte [Debugging Providers](debugging-providers.md).

## <a name="logging-and-tracing"></a>Registro em log e rastreamento

Os arquivos de log do WMI não existem mais; eles foram substituídos pelo [ETW (rastreamento de eventos para Windows)](/windows/desktop/ETW/event-tracing-portal). Para obter mais informações, consulte [rastrear atividade WMI](tracing-wmi-activity.md), [registrar em log a atividade WMI](logging-wmi-activity.md)e arquivos de [log WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Solução de problemas em scripts e aplicativos

O WMI contém um conjunto de classes para [solucionar problemas](wmi-troubleshooting-classes.md) de aplicativos cliente que usam provedores WMI. Para obter mais informações, consulte [Solucionando problemas de aplicativos cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Como os gravadores de provedor podem impedir problemas de WMI

Os gravadores de provedor podem impedir muitos problemas, que aparecem em mensagens de erro por meio do WMI, executando as seguintes ações:

-   Registrando seu provedor corretamente. Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).
-   Adicionar a instrução [**\# pragma Recover**](pragma-autorecover.md) ao arquivo formato MOF (MOF) que define suas classes de provedor.

Para obter mais informações, consulte [Depurando provedores](debugging-providers.md), [fornecendo dados para o WMI](providing-data-to-wmi.md)e [configuração do provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Acesso negado

Os erros de acesso negado que são relatados por scripts e aplicativos que acessam namespaces e dados do WMI geralmente se enquadram em três categorias. A tabela a seguir lista as três categorias de erros junto com problemas que podem causar os erros e as possíveis soluções.



| Erro                                                                                                                        | Possíveis problemas                                                                                                                                                                                                                                                                                                                                                                     | Solução                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema de firewall ou servidor não disponível.<br/>      | o computador realmente não existe ou o Firewall de Windows está bloqueando a conexão<br/>                                                                                                                                                                                                                                                                                        | conectando-se ao Vista: **netsh advfirewall firewall set rule group = "instrumentação de gerenciamento do windows (wmi)" novo enable = yes** conectando-se ao nível inferior: permitir a regra de "administração remota" no Windows firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0x80070005 **E \_ acesso \_ negado**<br/> Acesso negado pela segurança DCOM.<br/>                                       | O usuário não tem acesso remoto ao computador por meio do DCOM. Normalmente, os erros DCOM ocorrem durante a conexão com um computador remoto com uma versão diferente do sistema operacional.<br/>                                                                                                                                                                                          | Conceda ao usuário permissões de inicialização remota e ativação remota em dcomcnfg. Clique com o botão direito do mouse em Propriedades de Meu Computador >. Em segurança COM, clique em "Editar limites" para ambas as seções. Dê ao usuário que você deseja acesso remoto, inicialização remota e ativação remota. em seguida, vá para configuração do DCOM, localize "Instrumentação de Gerenciamento do Windows" e forneça ao usuário que você deseja inicialização remota e ativação remota. Para obter mais informações, consulte [conectando entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 **WBEM \_ E \_ acesso \_ negado**<br/> Acesso negado por um [ *provedor*](gloss-p.md)<br/> | O usuário não tem permissão para executar a operação no WMI. Isso pode acontecer quando você consulta determinadas classes como um usuário de direitos limitados, mas geralmente ocorre quando você tenta invocar métodos ou alterar instâncias WMI como um usuário de direitos limitados. O namespace ao qual você está se conectando está criptografado e o usuário está tentando se conectar com uma conexão não criptografada<br/> | conceda ao usuário acesso com o controle WMI (verifique se eles têm \_ acesso remoto definido como true) Conexão usando um cliente que dá suporte à criptografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   Normalmente, os erros DCOM ocorrem durante a conexão com um computador remoto com uma versão diferente do sistema operacional.

-   Os provedores também podem negar o acesso a dados em namespaces específicos ou podem exigir determinados níveis de segurança de conexão. Para obter mais informações, consulte [definindo segurança do processo do aplicativo cliente](setting-client-application-process-security.md) e [hospedagem e segurança do provedor](provider-hosting-and-security.md).

-   Os erros de acesso negado das alterações do firewall de conexão com a Internet (ICF).

    para obter mais informações, consulte [conectando por meio do Firewall Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

-   Um erro de acesso negado é retornado pela segurança DCOM quando um cliente de baixa integridade tenta acessar o WMI. por exemplo, um controle de ActiveX que está sendo executado no Internet Explorer, que tem o nível de segurança definido como baixo, não tem acesso para executar operações WMI locais.

    **Windows 7:** Usuários de baixa integridade têm permissões somente leitura para operações WMI locais.

## <a name="information-on-errors"></a>Informações sobre erros

Quando você recebe uma mensagem de erro do WMI, pode localizar a mensagem em [**constantes de erro do WMI**](wmi-error-constants.md) ou, para script, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). No entanto, as informações fornecidas pelo erro sozinhas normalmente são insuficientes para determinar o que está acontecendo. A corrupção do repositório WMI pode ser disfarçada como classes ou instâncias "não encontradas".

Para obter mais informações sobre erros do WMI:

-   Os logs do WMI rastreiam eventos de dentro do WMI Core e de provedores. Para obter mais informações, consulte [registrando em log a atividade do WMI](logging-wmi-activity.md).
-   Use as [classes de solução de problemas do WMI](wmi-troubleshooting-classes.md) para verificar o status interno do WMI ou receber notificações de eventos do provedor ou do serviço WMI. Para obter mais informações, consulte [configuração do provedor e solução de problemas de classes](provider-configuration-and-troubleshooting-classes.md) e solução de problemas de [aplicativos cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Rastreando a atividade WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrando em log a atividade WMI](logging-wmi-activity.md)
</dt> </dl>

 

