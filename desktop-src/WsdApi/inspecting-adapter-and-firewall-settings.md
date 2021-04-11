---
description: Um firewall configurado incorretamente pode causar falha em aplicativos WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Inspecionando as configurações de firewall e adaptador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296624"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Inspecionando as configurações de firewall e adaptador

Um firewall configurado incorretamente pode causar falha em aplicativos WSD. Este tópico fornece alguns procedimentos de solução de problemas a serem usados quando clientes e hosts WSD não podem ver uns aos outros na rede. As configurações de firewall devem ser inspecionadas antes de usar qualquer outro procedimento de solução de problemas de aplicativo.

**Para inspecionar as configurações de adaptador e firewall**

1.  Verifique se a exceção de **descoberta de rede** está habilitada.
2.  Verifique se não há regras de firewall específicas do aplicativo bloqueando o aplicativo.
3.  Habilite explicitamente as portas usadas para descoberta e troca de metadados.
4.  Desabilite o firewall e teste o aplicativo novamente.
    > [!Note]  
    > O firewall deve ser habilitado novamente após a conclusão desta etapa.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Verificando se a exceção de descoberta de rede está habilitada

Se algum aplicativo WS-Discovery estiver em execução, a exceção de firewall de **descoberta de rede** deverá ser permitida.

**Para habilitar a exceção de firewall de descoberta de rede**

1.  Clique em **Iniciar**, **executar** e digite **firewall.cpl**. Isso abre o miniaplicativo do **painel de controle do firewall do Windows** .
2.  Escolha **permitir um programa por meio do firewall do Windows**.
3.  Na guia **exceções** , marque a caixa de seleção **descoberta de rede** .
4.  Clique em **OK** para fechar o miniaplicativo firewall.

Teste o programa novamente depois de fazer essa alteração no firewall. Se o programa agora funciona com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="checking-for-application-specific-firewall-rules"></a>Verificando regras de firewall específicas do aplicativo

A configuração avançada do firewall do Windows pode ocorrer em um snap-in do Microsoft Management Control (MMC) chamado **Firewall do Windows com segurança avançada**. Esse snap-in pode ser usado para solucionar problemas de firewall suspeitos.

Os desenvolvedores podem usar as APIs [Firewall do Windows com segurança avançada](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) para criar regras de firewall que se aplicam aos seus aplicativos WSD. Especificamente, o método [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) da interface [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) pode ser usado para adicionar uma nova regra de firewall. Se as regras de firewall forem criadas incorretamente, os clientes e hosts não poderão ver um ao outro na rede.

**Para verificar se há regras de firewall específicas do aplicativo**

1.  Clique em **Iniciar**, **executar** e digite **WF. msc**.
2.  Procure regras específicas do aplicativo que possam estar bloqueando o tráfego. Para obter mais informações, consulte [Firewall do Windows com segurança avançada-ferramentas de diagnóstico e solução de problemas](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Remova as regras específicas do aplicativo.

Se nenhuma regra específica do aplicativo for encontrada, vá para a próxima etapa. Se uma regra específica do aplicativo for encontrada e removida, teste o programa novamente depois de fazer a alteração do firewall. Se o programa agora funciona com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Habilitando as portas usadas para descoberta e troca de metadados

WS-Discovery usa a porta UDP 3702 para troca de mensagens. Além disso, as portas TCP 5357 e 5358 às vezes são usadas para troca de metadados. Essas portas podem ser abertas explicitamente no firewall usando os procedimentos descritos em [abrir uma porta no firewall do Windows](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).

Teste o programa novamente depois de fazer essa alteração no firewall. Se o programa agora funciona com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="disabling-the-firewall"></a>Desabilitando o firewall

O Firewall do Windows pode ser desabilitado para ajudar a solucionar problemas suspeitos. Outros firewalls aplicáveis (como o firewall em um roteador) também podem ser desabilitados para fins de solução de problemas. Para obter informações sobre como habilitar e desabilitar o Firewall do Windows, consulte [Ativar ou](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)desativar o Firewall do Windows.

Teste o aplicativo novamente depois de desabilitar os firewalls aplicáveis. Se o programa agora funciona com êxito, o firewall estava bloqueando o tráfego. Há algumas causas possíveis do tráfego bloqueado.

-   As exceções específicas do aplicativo bloquearam o tráfego. Verifique as regras de firewall específicas do aplicativo, conforme descrito acima.
-   O dispositivo demorou muito tempo para responder às solicitações de UDP. O Firewall do Windows pode bloquear respostas UDP que retornam mais de 4 segundos depois que a solicitação inicial foi enviada. Continue a solução de problemas seguindo os procedimentos fornecidos em como [usar um host genérico e um cliente para a descoberta de WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) para ver se o problema é reproduzido com um host que responde em menos de 4 segundos.

Se o aplicativo ainda falhar depois que o firewall for desabilitado, o firewall não estará causando a falha do aplicativo. Habilite novamente os firewalls e continue a solução de problemas seguindo os procedimentos fornecidos no [uso de um host genérico e cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Os firewalls sempre devem ser habilitados novamente após a conclusão da solução de problemas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
