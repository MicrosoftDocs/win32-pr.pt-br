---
title: Usando o netsh para gerenciar rastreamentos
description: no Windows 7, netsh.exe pode ser usado em um prompt de comando para habilitar e configurar os rastreamentos de rede. Esta seção descreve alguns dos comandos netsh.exe que podem ajudar na solução de problemas de rastreamento, incluindo a nova funcionalidade de rastreamento do netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07c4be1c89c496245cb67bec4aef8614f5efef5db003e6c79cef2e54314c3071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133249"
---
# <a name="using-netsh-to-manage-traces"></a>Usando o netsh para gerenciar rastreamentos

no Windows 7, netsh.exe pode ser usado em um prompt de comando para habilitar e configurar os rastreamentos de rede. Esta seção descreve alguns dos comandos netsh.exe que podem ajudar na solução de problemas de rastreamento, incluindo a nova funcionalidade de **rastreamento do netsh** . Observe que os comandos netsh devem ser executados em um prompt de comandos com privilégios elevados.

## <a name="collecting-traces"></a>Coleta de rastreamentos

Cenários são conjuntos predefinidos de provedores de rastreamento que podem ser habilitados para solução de problemas. Para exibir a lista de cenários relacionados à rede disponíveis, digite **netsh trace show Scenarios** (**netsh trace show Providers** lista cada um dos provedores disponíveis, incluindo aqueles que não são relevantes para a rede).

Quando você tiver identificado um cenário que se pareça relevante para seus problemas, poderá ver uma lista de todos os provedores incluídos nesse cenário. Por exemplo, para ver todos os provedores habilitados no cenário InternetClient, digite **netsh trace show Scenario internetclient**.

Você pode iniciar um rastreamento para todos os provedores em um determinado cenário ou conjunto de cenários. Por exemplo, para iniciar um rastreamento para todos os provedores habilitados no cenário InternetClient, digite **netsh trace Start Scenario = internetclient**. Para capturar provedores de mais de um cenário, você pode especificar todos os cenários apropriados, como o cenário de **início de rastreamento netsh = filesharing Scenario = DirectAccess**. Observe que apenas uma sessão de rastreamento pode ser habilitada por vez; Não é possível capturar simultaneamente informações de rastreamento de diferentes conjuntos de provedores em arquivos separados.

Você também pode iniciar um rastreamento para provedores adicionais não incluídos nesse cenário específico. Por exemplo, você pode querer iniciar rastreamentos para todos os provedores habilitados no cenário de WLAN e também o provedor DHCP. para fazer isso, digite **netsh trace start cenário = wlan provider = Microsoft-Windows-Dhcp-Client**.

Você também pode ver mais detalhes sobre um provedor específico digitando **netsh trace show provedor** seguido pelo nome do provedor.

Para ver todas as opções e filtros disponíveis, você pode digitar **netsh trace Start/?**.

Para interromper o rastreamento, digite **netsh trace stop**.

## <a name="using-the-output-files"></a>Usando os arquivos de saída

Quando o rastreamento é interrompido, dois arquivos são gerados por padrão: um arquivo de log de rastreamento de eventos (ETL) e um arquivo de .cab.

Os eventos de rastreamento são coletados no arquivo ETL, que pode ser exibido usando ferramentas como Monitor de Rede. O arquivo ETL será nomeado NetTrace. etl por padrão ou você poderá especificar um nome diferente, incluindo **TraceFile = filename. etl** ao iniciar o rastreamento.

O arquivo de .cab contém informações avançadas sobre o software e o hardware no sistema, como as informações do adaptador, a compilação, o sistema operacional e as configurações sem fio. O arquivo de .cab será nomeado nettrace.cab por padrão, a menos que outro nome tenha sido especificado, conforme indicado acima.

Esse .cab arquivo conterá dois arquivos, que sempre terão o mesmo nome. Report. etl é outra cópia das mesmas informações incluídas no NetTrace. etl. O arquivo l report.htminclui informações adicionais sobre os eventos de rastreamento e as outras informações coletadas. Para receber a maioria dos detalhes disponíveis, inclua o comando **Report = Yes** ao iniciar um rastreamento.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Usando filtros para reduzir a quantidade de dados no arquivo de rastreamento de ETL

Quando as capturas acontecem durante um longo período de tempo, o arquivo de rastreamento ETL pode ficar muito grande. Em cenários em que vários provedores estão habilitados, resultando em tráfego alto, restrições de buffer ETW podem fazer com que alguns rastreamentos sejam removidos. Além dessa consideração, a redução da quantidade de dados no arquivo de rastreamento ETL pode ajudar a facilitar a solução de problemas, reduzindo a quantidade de dados a serem examinados.

Os filtros de rastreamento do netsh podem ser usados para reduzir o tamanho do arquivo de rastreamento de ETL. Esses filtros de rastreamento são níveis de ETW e palavras-chave que podem ser aplicados a provedores individuais.

Para ver uma lista de filtros que podem ser aplicados, digite **netsh trace Start/?**

um exemplo de filtro é **netsh trace start InternetClient provedor = Microsoft-Windows-TCPIP nível = 5 palavras-chave = ut: ReceivePath, ut: SendPath**.

Neste exemplo, o nível é definido como 5, o que significa que o número máximo de eventos será mostrado. A tabela a seguir mostra as configurações disponíveis:



| Nível      | Configuração              | Descrição                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Crítico      | Somente eventos críticos serão mostrados.                                        |
| 2     | Erros        | Eventos e erros críticos serão mostrados.                                  |
| 3     | Avisos      | Eventos críticos, erros e avisos serão mostrados.                       |
| 4     | Informativo | Eventos críticos, erros, avisos e eventos informativos serão mostrados. |
| 5     | Detalhado       | Todos os eventos serão mostrados.                                                  |



 

As palavras-chave **UT: ReceivePath** e **UT: SentPath** filtra os eventos para mostrar somente os eventos rastreados no caminho de recebimento ou de envio. Uma lista completa de palavras-chave para um provedor específico pode ser encontrada digitando o **provedor netsh trace show** seguido pelo nome do provedor. por exemplo, digitar **netsh trace show provedor microsoft-Windows-TCPIP** exibirá informações sobre o provedor Microsoft-Windows-tcpip, incluindo uma lista de palavras-chave.

O netsh também dá suporte à funcionalidade de filtragem de pacotes (semelhante a Monitor de Rede) quando a captura de pacotes está ativada (definindo **Capture = Yes**). A filtragem de pacotes pode ser usada para capturar um número limitado de pacotes em um arquivo de rastreamento. Por exemplo, **netsh trace Start Capture = Sim IPv4. Address = = x.** x. x. x, em que x. x. x. x é o endereço IP, capturará somente os pacotes com o tráfego IPv4 com esse endereço de origem ou de destino específico.

Para obter informações adicionais sobre como usar a filtragem de pacotes, você pode digitar **netsh trace show capturefilterHelp**.

 

 




