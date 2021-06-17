---
description: Saiba mais sobre como inspecionar rastreamentos de rede para troca de metadados HTTP. Use um analisador de pacotes de rede que exibe pacotes brutos.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Inspecionando rastreamentos de rede para troca de metadados HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e653b0852f84382873973cd63fbd3223a245dd4
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262678"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Inspecionando rastreamentos de rede para troca de metadados HTTP

Qualquer analisador de pacote de rede que possa exibir pacotes brutos pode ser usado para inspecionar solicitações de troca de metadados HTTP. Monitor de Rede da Microsoft 3 (Netmon) é recomendado. Para obter mais informações sobre o Netmon, consulte [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).

Esse procedimento de diagnóstico pode não ser tão útil para clientes e hosts que usam um canal seguro para comunicações porque o conteúdo da mensagem é criptografado.

**Para inspecionar rastreamentos de rede para troca de metadados HTTP**

1.  Configure o host e o cliente para executar na rede (ou seja, certifique-se de que o host e o cliente operarão em diferentes máquinas).
2.  Instale o analisador de pacotes (Netmon) no cliente ou no host.
3.  Configure o analisador de pacotes para capturar o tráfego no adaptador de rede que conecta o host e o cliente.
4.  Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de Rede.
5.  Filtre os resultados para isolar o tráfego WS-Discovery troca de metadados. Para exibir filtros Netmon de exemplo, consulte [Baixando o Netmon e exemplos de filtros DPWS](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Esta etapa é opcional.

     

6.  Verifique se as mensagens enviadas entre o cliente e o host atendem aos requisitos básicos de tráfego.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verificar se as mensagens atendem aos requisitos de tráfego

Os clientes e hosts WSDAPI devem enviar mensagens em conformidade com os critérios a seguir. Para obter informações gerais sobre padrões de mensagem, consulte Descoberta e padrões de mensagens [de troca de metadados](discovery-and-metadata-exchange-message-patterns.md).

-   As mensagens devem atender aos requisitos de tráfego fornecidos no tópico Inspecionando rastreamentos de rede para descoberta de [WS-Discovery UDP,](inspecting-network-traces-for-udp-ws-discovery.md)a menos que seja absolutamente certo WS-Discovery está sendo usado para troca de metadados.
-   Uma conexão TCP deve ser estabelecida entre o cliente e o primeiro endereço de transporte fornecido no elemento **XAddrs** de uma [mensagem ProbeMatches](probematches-message.md) [ou ResolveMatches.](resolvematches-message.md) A lista a seguir mostra uma troca de pacotes típica usada para estabelecer uma conexão TCP.
    -   O cliente envia um pacote TCP SYN para o host em uma porta especificada.
    -   O host envia um pacote TCP SYN/ACK para o cliente.
    -   O cliente envia um pacote TCP ACK para o host em uma porta especificada.

    Depois que o cliente enviar um pacote TCP ACK, a conexão TCP será estabelecida. Observe que essa troca de mensagens não ocorrerá se uma conexão TCP tiver sido estabelecida anteriormente.
-   O cliente deve enviar uma [solicitação](get--metadata-exchange--http-request-and-message.md) HTTP e uma mensagem válidas.
-   O host deve estar escutando no caminho da URL especificado na [solicitação Obter](get--metadata-exchange--http-request-and-message.md) HTTP.
-   O **elemento To** de uma mensagem [Obter](get--metadata-exchange--http-request-and-message.md) metadados deve estar presente e não vazio. O valor do elemento **To** deve corresponder a um dos endereços de ponto de extremidade do host. O endereço do ponto de extremidade de um host normalmente é anunciado em uma [mensagem ProbeMatches](probematches-message.md) [ou ResolveMatches.](resolvematches-message.md)
-   O host deve enviar um cabeçalho de resposta HTTP válido. Se a solicitação inicial tiver sido bem-sucedida, o cabeçalho de resposta deverá conter o código de status HTTP/1.1 200.
-   O host deve enviar uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) válida.
-   O **elemento RelatesTo** de uma [mensagem GetResponse](getresponse--metadata-exchange--message.md) deve estar presente e não deve estar vazio. Seu valor deve corresponder ao valor do **elemento MessageId** da mensagem [Get](get--metadata-exchange--http-request-and-message.md) correspondente.

Se as solicitações HTTP ou mensagens de troca de metadados enviadas pelo programa não estão em conformidade com esses requisitos de tráfego, a causa do problema foi identificada com êxito e nenhuma etapa de solução de problemas é necessária. Reescreva o programa para que ele gere mensagens e solicitações compatíveis e teste novamente o programa.

Se a origem do problema ainda não puder ser identificada, entre em contato com o suporte da Microsoft para saber mais. Antes de entrar em contato com o suporte, colete os arquivos de log apropriados para ajudar a identificar a causa raiz do problema. Para obter mais informações, consulte [Habilitando o rastreamento WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Baixando o Netmon e exemplos de filtros DPWS](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



