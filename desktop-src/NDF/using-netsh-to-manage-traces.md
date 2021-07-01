---
title: Usando o Netsh para gerenciar rastreamentos
description: No Windows 7, netsh.exe pode ser usado em um prompt de comando para habilitar e configurar rastreamentos de rede. Esta seção descreve alguns dos comandos netsh.exe que podem ajudar na solução de problemas de rastreamento, incluindo a nova funcionalidade de rastreamento netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119021"
---
# <a name="using-netsh-to-manage-traces"></a>Usando o Netsh para gerenciar rastreamentos

No Windows 7, netsh.exe pode ser usado em um prompt de comando para habilitar e configurar rastreamentos de rede. Esta seção descreve alguns dos comandos netsh.exe que podem ajudar na solução de problemas de rastreamento, incluindo a nova **funcionalidade de rastreamento netsh.** Observe que os comandos netsh devem ser executados em um prompt de comando com elevação.

## <a name="collecting-traces"></a>Coletando rastreamentos

Os cenários são conjuntos predefinidos de provedores de rastreamento que podem ser habilitados para solução de problemas. Para exibir a lista de cenários disponíveis relacionados à rede, digite **cenários netsh trace show** **(provedores netsh trace show** lista cada um dos provedores disponíveis, incluindo aqueles que não são relevantes para a rede).

Quando você identificar um cenário que parece relevante para seus problemas, poderá ver uma lista de todos os provedores incluídos nesse cenário. Por exemplo, para ver todos os provedores habilitados no cenário InternetClient, digite **netsh trace show scenario internetclient**.

Você pode iniciar um rastreamento para todos os provedores em um determinado cenário ou conjunto de cenários. Por exemplo, para iniciar um rastreamento para todos os provedores habilitados no cenário InternetClient, digite **netsh trace start scenario=internetclient**. Para capturar provedores para mais de um cenário, você pode especificar todos os cenários apropriados, como **netsh trace start scenario=FileSharing scenario=DirectAccess**. Observe que apenas uma sessão de rastreamento pode ser habilitada por vez; Não é possível capturar simultaneamente informações de rastreamento de diferentes conjuntos de provedores em arquivos separados.

Você também pode iniciar um rastreamento para provedores adicionais não incluídos nesse cenário específico. Por exemplo, talvez você queira iniciar rastreamentos para todos os provedores habilitados no cenário WLAN e também o provedor DHCP. Para fazer isso, digite **netsh trace start scenario=wlan provider=Microsoft-Windows-Dhcp-Client**.

Você também pode ver mais detalhes sobre um provedor específico digitando **netsh trace show provider** seguido pelo nome do provedor.

Para ver todas as opções e filtros disponíveis, digite **netsh trace start /?**.

Para interromper o rastreamento, digite **netsh trace stop**.

## <a name="using-the-output-files"></a>Usando os arquivos de saída

Quando o rastreamento é interrompido, dois arquivos são gerados por padrão: um arquivo ETL (Log de Rastreamento de Eventos) e um .cab arquivo.

Os eventos de rastreamento são coletados no arquivo ETL, que pode ser exibido usando ferramentas como Monitor de Rede. O arquivo ETL será nomeado nettrace.etl por padrão ou você poderá especificar um nome diferente incluindo **tracefile=filename.etl** ao iniciar o rastreamento.

O .cab arquivo contém informações sofisticadas sobre o software e o hardware no sistema, como as informações de adaptador, build, sistema operacional e configurações sem fio. O .cab será nomeado como nettrace.cab por padrão, a menos que outro nome tenha sido especificado, conforme indicado acima.

Esse .cab arquivo conterá dois arquivos, que sempre terão o mesmo nome. Report.etl é outra cópia das mesmas informações incluídas em nettrace.etl. O report.html inclui informações adicionais sobre os eventos de rastreamento e as outras informações coletadas. Para receber os detalhes mais disponíveis, inclua o relatório de **comando = sim** ao iniciar um rastreamento.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Usando filtros para reduzir a quantidade de dados no arquivo de rastreamento ETL

Quando as capturas ocorrem por um longo período de tempo, o arquivo de rastreamento de ETL pode se tornar muito grande. Em cenários em que vários provedores estão habilitados, resultando em alto tráfego, as restrições de buffer ETW podem fazer com que alguns rastreamentos sejam descartados. Além dessa consideração, reduzir a quantidade de dados no arquivo de rastreamento de ETL pode ajudar a facilitar a solução de problemas, reduzindo a quantidade de dados a ser revisada.

Os filtros de rastreamento netsh podem ser usados para reduzir o tamanho do arquivo de rastreamento de ETL. Esses filtros de rastreamento são níveis ETW e palavras-chave que podem ser aplicados a provedores individuais.

Para ver uma lista de filtros que podem ser aplicados, digite **netsh trace start /?**

Um exemplo de um filtro é **netsh trace start InternetClient provider=Microsoft-Windows-TCPIP level=5 keywords=ut:ReceivePath,ut:SendPath**.

Neste exemplo, o nível é definido como 5, o que significa que o número máximo de eventos será mostrado. A tabela a seguir mostra as configurações disponíveis:



| Level      | Configuração              | Descrição                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Crítico      | Somente eventos críticos serão mostrados.                                        |
| 2     | Errors        | Eventos críticos e erros serão mostrados.                                  |
| 3     | Warnings      | Eventos críticos, erros e avisos serão mostrados.                       |
| 4     | Informativo | Eventos críticos, erros, avisos e eventos informacionais serão mostrados. |
| 5     | Detalhado       | Todos os eventos serão mostrados.                                                  |



 

As **palavras-chave ut:ReceivePath** e **ut:SentPath** filtram os eventos para mostrar somente os eventos rastreados no caminho de recebimento ou envio. Uma lista completa de palavras-chave para um provedor específico pode ser encontrada digitando **netsh trace show provider** seguido pelo nome do provedor. Por exemplo, digitar **netsh trace show provider Microsoft-Windows-TCPIP** exibirá informações sobre o provedor Microsoft-Windows-TCPIP, incluindo uma lista de palavras-chave.

O Netsh também dá suporte à funcionalidade de filtragem de pacotes (semelhante ao Monitor de Rede) quando a captura de pacotes está 100000001(captura **de configuração = sim).** A filtragem de pacotes pode ser usada para capturar um número limitado de pacotes em um arquivo de rastreamento. Por exemplo, **netsh trace start capture = yes ipv4.address == x.x.x.x.x** , em que x.x.x.x é o endereço IP, apenas capturará pacotes com tráfego ipv4 com esse endereço de origem ou destino específico.

Para obter informações adicionais sobre como usar a filtragem de pacotes, digite **netsh trace show capturefilterHelp**.

 

 




