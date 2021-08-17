---
description: Um firewall configurado indeformado pode fazer com que os aplicativos WSD falhem.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Inspecionando adaptador e firewall Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ea14051ac65dbd0b749fa00566afc9ed82e5571f6027dafa003e12013888b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130778"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Inspecionando adaptador e firewall Configurações

Um firewall configurado indeformado pode fazer com que os aplicativos WSD falhem. Este tópico fornece alguns procedimentos de solução de problemas a usar quando os clientes e hosts do WSD não podem se ver na rede. As configurações de firewall devem ser inspecionadas antes de usar qualquer outro procedimento de solução de problemas de aplicativo.

**Para inspecionar as configurações de adaptador e firewall**

1.  Verifique se a **exceção descoberta de** rede está habilitada.
2.  Verifique se não há regras de firewall específicas do aplicativo bloqueando o aplicativo.
3.  Habilita explicitamente as portas usadas para descoberta e troca de metadados.
4.  Desabilite o firewall e teste novamente o aplicativo.
    > [!Note]  
    > O firewall deve ser habilitado de modo reabilitar após a conclusão desta etapa.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Verificando se a exceção de Descoberta de Rede está habilitada

Se algum WS-Discovery aplicativos estiver em execução, a **exceção** de firewall de Descoberta de Rede deverá ser permitida.

**Para habilitar a exceção de firewall de Descoberta de Rede**

1.  Clique **em** Iniciar , **clique em Executar** e digite **firewall.cpl**. Isso abre o **Windows firewall Painel de Controle** applet.
2.  Escolha **Permitir um programa por meio Windows Firewall**.
3.  Na guia **Exceções,** marque a caixa **de seleção Descoberta** de Rede.
4.  Clique **em OK** para fechar o applet do firewall.

Teste novamente o programa depois de fazer essa alteração de firewall. Se o programa agora funcionar com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="checking-for-application-specific-firewall-rules"></a>Verificando regras de firewall específicas do aplicativo

A configuração avançada Windows Firewall pode ocorrer em um snap-in do MMC (Controle de Gerenciamento Microsoft) chamado **Windows Firewall com Segurança Avançada**. Esse snap-in pode ser usado para solucionar problemas de firewall suspeitos.

Os desenvolvedores podem usar [o firewall Windows com](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) APIs de Segurança Avançada para criar regras de firewall que se aplicam a seus aplicativos WSD. Especificamente, o [**método Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) da interface [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) pode ser usado para adicionar uma nova regra de firewall. Se as regras de firewall são criadas incorretamente, os clientes e hosts podem não conseguir se ver na rede.

**Para verificar se há regras de firewall específicas do aplicativo**

1.  Clique **em** Iniciar , **clique em** Executar e digite **wf.msc**.
2.  Procure regras específicas do aplicativo que podem estar bloqueando o tráfego. Para obter mais informações, consulte Windows Firewall com Segurança Avançada [– Ferramentas de Diagnóstico e Solução de Problemas](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Remover regras específicas do aplicativo.

Se nenhuma regra específica do aplicativo for encontrada, vá para a próxima etapa. Se uma regra específica do aplicativo foi encontrada e removida, teste novamente o programa depois de fazer a alteração do firewall. Se o programa agora funcionar com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Habilitando as portas usadas para descoberta e troca de metadados

WS-Discovery usa a porta UDP 3702 para troca de mensagens. Além disso, as portas TCP 5357 e 5358 às vezes são usadas para troca de metadados. Essas portas podem ser abertas explicitamente no firewall usando os procedimentos descritos em [Abrir uma porta no firewall Windows .](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)

Teste novamente o programa depois de fazer essa alteração de firewall. Se o programa agora funcionar com êxito, a causa do problema foi identificada e nenhuma outra etapa de solução de problemas é necessária. Caso contrário, vá para a próxima etapa.

## <a name="disabling-the-firewall"></a>Desabilitando o firewall

O Windows firewall pode ser desabilitado para ajudar a solucionar problemas suspeitos. Outros firewalls aplicáveis (como o firewall em um roteador) também podem ser desabilitados para fins de solução de problemas. Para obter informações sobre como habilenciar e desabilitar o firewall Windows, consulte Ativar ou desativar o [firewall Windows aplicativo.](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)

Teste novamente o aplicativo depois de desabilitar os firewalls aplicáveis. Se o programa agora funciona com êxito, o firewall estava bloqueando o tráfego. Há algumas causas possíveis de tráfego bloqueado.

-   Exceções específicas do aplicativo bloquearam o tráfego. Verifique se há regras de firewall específicas do aplicativo, conforme descrito acima.
-   O dispositivo demorou muito para responder a solicitações UDP. O Windows Firewall pode bloquear as respostas UDP que retornam mais de 4 segundos após a solicitação inicial ter sido enviada. Continue a solução de problemas seguindo os procedimentos determinados em Usando um host genérico e um cliente para [UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) para ver se o problema é reproduzido com um host que responde em menos de 4 segundos.

Se o aplicativo ainda falhar depois que o firewall estiver desabilitado, o firewall não causará a falha do aplicativo. Reabilitar os firewalls e continuar a solução de problemas seguindo os procedimentos determinados em Usando um host genérico e [um cliente para ODP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Os firewalls sempre devem ser habilitados de modo reabilitar depois que a solução de problemas for concluída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
