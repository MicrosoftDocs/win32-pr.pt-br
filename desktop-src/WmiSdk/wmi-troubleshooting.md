---
description: Ao acessar dados locais ou remotos do WMI em um aplicativo ou script, você pode encontrar erros que variam de classes ausentes ao acesso negado. Os provedores também têm opções de depuração e classes de solução de problemas disponíveis.
ms.assetid: b0aecdf6-ec30-49be-af4e-7eac5d124057
ms.tgt_platform: multiple
title: Solução de problemas de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58919617c663b52ffb840b3c3382b5707f0a305e
ms.sourcegitcommit: a3e96b6c9c6a3fb629e760dd6cc6327f9e4b62b6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/27/2021
ms.locfileid: "114714798"
---
# <a name="wmi-troubleshooting"></a>Solução de problemas de WMI

Ao acessar dados locais ou remotos do WMI em um aplicativo ou script, você pode encontrar erros que variam de classes ausentes ao acesso negado. Os provedores também têm opções de depuração e classes de solução de problemas disponíveis.

> [!Note]  
> A documentação a seguir é direcionada para desenvolvedores e administradores de IT. Se você for um usuário final que passou por uma mensagem [](https://support.microsoft.com/) de erro referente ao WMI, vá para o Suporte da Microsoft e pesquise o código de erro que você vê na mensagem de erro. Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10))

 

## <a name="wmi-diagnosis-utility"></a>Utilitário de Diagnóstico WMI

O utilitário de diagnóstico WMI (WMIDiag.exe) não tem mais suporte a partir do Windows 8 e Windows Server 2012.

**Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008: **

Se o WMI retornar mensagens de erro, esteja ciente de que elas podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstâncias, não exclua o repositório WMI como uma primeira ação porque a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.

Para obter mais informações sobre a origem do problema, você pode baixar e executar a [Utilitário de Diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de linha de comando de diagnóstico. Essa ferramenta produz um relatório que geralmente pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft a ajudá-lo. Você pode baixar o Utilitário de Diagnóstico WMI no Centro [de Download.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

Os autores de provedor também podem encontrar problemas de depuração, a menos que você esteja escrevendo [*um provedor desaparado.*](gloss-d.md) Para obter mais informações, consulte [Provedores de depuração](debugging-providers.md).

## <a name="logging-and-tracing"></a>Registro em log e rastreamento

Os arquivos de log do WMI não existem mais; eles foram substituídos pelo [Rastreamento de Eventos Windows (ETW).](/windows/desktop/ETW/event-tracing-portal) Para obter mais informações, consulte [Rastreamento da atividade WMI,](tracing-wmi-activity.md) [Atividade WMI de](logging-wmi-activity.md)log e Arquivos de log [WMI](wmi-log-files.md).

## <a name="troubleshooting-in-scripts-and-applications"></a>Solução de problemas em scripts e aplicativos

O WMI contém um conjunto de classes para solucionar [problemas de](wmi-troubleshooting-classes.md) aplicativos cliente que usam provedores WMI. Para obter mais informações, consulte [Solução de problemas de aplicativos cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="how-provider-writers-can-prevent-wmi-problems"></a>Como os autores de provedores podem evitar problemas de WMI

Os autores do provedor podem evitar muitos problemas, que aparecem em mensagens de erro por meio do WMI, executando as seguintes ações:

-   Registrar seu provedor corretamente. Para obter mais informações, [consulte Registrando um provedor](registering-a-provider.md).
-   Adicionar a [**\# instrução pragma autorecover**](pragma-autorecover.md) ao arquivo Managed Object Format (MOF) que define suas classes de provedor.

Para obter mais informações, consulte [Provedores de depuração](debugging-providers.md), Fornecendo dados ao [WMI](providing-data-to-wmi.md)e Configuração do Provedor e Classes [de solução de problemas](provider-configuration-and-troubleshooting-classes.md).

## <a name="access-denied"></a>Acesso negado

Os erros de acesso negado relatados por scripts e aplicativos que acessam namespaces e dados WMI geralmente se enquadram em três categorias. A tabela a seguir lista as três categorias de erros, juntamente com problemas que podem causar erros e possíveis soluções.



| Erro                                                                                                                        | Possíveis problemas                                                                                                                                                                                                                                                                                                                                                                     | Solução                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x800706BA `HRESULT_FROM_WIN32(RPC_S_SERVER_UNAVAILABLE)`<br/> Problema de firewall ou servidor não disponível.<br/>      | O computador realmente não existe ou o firewall Windows está bloqueando a conexão<br/>                                                                                                                                                                                                                                                                                        | Conectando-se ao Vista: **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes** Connecting to downlevel: Allow the "Remote Administration" rule in Windows Firewall.<br/>                                                                                                                                                                                                                                                                                                            |
| 0X80070005 **ACESSO \_ E \_ NEGADO**<br/> Acesso negado pela segurança do DCOM.<br/>                                       | O usuário não tem acesso remoto ao computador por meio do DCOM. Normalmente, ocorrem erros de DCOM ao se conectar a um computador remoto com uma versão diferente do sistema operacional.<br/>                                                                                                                                                                                          | Dê ao usuário permissões de Início Remoto e Ativação Remota em dcomcnfg. Clique com o botão direito do Meu Computador > Propriedades. Em Segurança COM, clique em "Editar Limites" para ambas as seções. Dê ao usuário que você deseja acesso remoto, início remoto e ativação remota. Em seguida, acesse Configuração do DCOM, encontre "instrumentação de gerenciamento Windows" e dê ao usuário que você deseja Iniciar Remotamente e Ativação Remota. Para obter mais informações, consulte [Conectando-se entre diferentes sistemas operacionais](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)<br/> |
| 0x80041003 ACESSO **AO WBEM \_ E \_ \_ NEGADO**<br/> Acesso negado por um [ *provedor*](gloss-p.md)<br/> | O usuário não tem permissão para executar a operação no WMI. Isso pode acontecer quando você consulta determinadas classes como um usuário com direitos baixos, mas geralmente ocorre quando você tenta invocar métodos ou alterar instâncias WMI como um usuário com direitos baixos. O namespace ao que você está se conectando é criptografado e o usuário está tentando se conectar com uma conexão não criptografada<br/> | Dê ao usuário acesso com o controle WMI (certifique-se de que ele tenha Acesso Remoto definido como true) Conexão usando um cliente que dá \_ suporte à criptografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

-   Normalmente, ocorrem erros de DCOM ao se conectar a um computador remoto com uma versão diferente do sistema operacional.

-   Os provedores também podem negar o acesso a dados em namespaces específicos ou podem exigir determinados níveis de segurança de conexão. Para obter mais informações, consulte [Configurando a segurança do processo de aplicativo cliente](setting-client-application-process-security.md) e a [hospedagem e a segurança do provedor.](provider-hosting-and-security.md)

-   Erros de acesso negado de alterações do Firewall de Conexão com a Internet (ICF).

    Para obter mais informações, consulte [Conectando-se Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)do .

-   Um erro de acesso negado é retornado pela segurança do DCOM quando um cliente de baixa integridade tenta acessar o WMI. Por exemplo, um ActiveX que está em execução no Internet Explorer, que tem o nível de segurança definido como baixo, não tem acesso para executar operações WMI locais.

    **Windows 7:** Usuários de baixa integridade têm permissões somente leitura para operações WMI locais.

## <a name="information-on-errors"></a>Informações sobre erros

Ao receber uma mensagem de erro do WMI, você pode localizar a mensagem em [**Constantes**](wmi-error-constants.md) de Erro WMI ou, para scripts, [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum). No entanto, as informações fornecidas apenas pelo erro são normalmente insuficientes para determinar o que está acontecendo. A corrupção do repositório WMI pode ser mascarada como classes ou instâncias "não encontradas".

Para obter mais informações sobre erros de WMI:

-   Os logs do WMI acompanham eventos de dentro do núcleo do WMI e de provedores. Para obter mais informações, consulte [Registrando em log a atividade WMI](logging-wmi-activity.md).
-   Use as [Classes de Solução de Problemas WMI](wmi-troubleshooting-classes.md) para verificar o status interno do WMI ou receber notificações de eventos de serviço WMI ou provedor. Para obter mais informações, consulte [Configuração do provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md) e Solução de problemas de [aplicativos cliente WMI](troubleshooting-wmi-client-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Atividade WMI de rastreamento](tracing-wmi-activity.md)
</dt> <dt>

[Registrando em log a atividade WMI](logging-wmi-activity.md)
</dt> </dl>

 

