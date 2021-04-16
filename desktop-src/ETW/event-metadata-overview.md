---
description: 'Esta é uma visão geral do que esperar para a jornada de ponta a ponta de um evento para cada uma das quatro tecnologias de rastreamento fornecidas pela Microsoft: TraceLogging, com base em manifesto, WPP e MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Visão geral dos metadados do evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c16853ef2639fd560f5b5da30447556119ec877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460970"
---
# <a name="event-metadata-overview"></a>Visão geral dos metadados do evento

Esta é uma visão geral do que esperar para a jornada de ponta a ponta de um evento para cada uma das quatro tecnologias de rastreamento fornecidas pela Microsoft: [TraceLogging](../tracelogging/trace-logging-about.md), [com base em manifesto](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)e [MOF](tracing-events.md). Ele se aproxima do problema em relação à carga de um evento individual e aos metadados que o acompanham, tornando possível decodificar posteriormente o evento em partes sensatas de dados. Compreender a jornada de cada parte de um evento é importante ao escolher qual tecnologia de rastreamento é apropriada para um projeto. Não há nenhuma solução de tamanho único para rastreamento.

## <a name="event-payloads"></a>Cargas de evento

Para qualquer uma das tecnologias de rastreamento fornecidas pela Microsoft, ao chamar o comando Write (por exemplo, [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para a instância baseada em manifesto ou [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para TraceLogging), os dados fornecidos para o evento em tempo de execução são dobrados em um blob binário contíguo chamado carga do evento. Isso é separado do esquema de evento ou dos metadados de evento (discutidos abaixo), que descreve o layout desse blob binário para ferramentas de decodificação. O quão exatamente a geração da carga do evento ocorre varia dependendo da tecnologia de rastreamento usada e, por fim, se o evento é clássico (estilo [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) ) ou moderno (estilo **EventWrite** ).

Para eventos clássicos, o sinalizador no [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) é passado para [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) que determina como isso ocorre:

\- Se **o \_ sinalizador WNODE \_ usar o \_ MOF \_ PTR** for especificado, uma matriz de [**\_ campos MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) seguirá o [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) na memória. O tempo de execução do ETW concatenará os dados do evento conforme especificado nesses campos para formar a carga do evento.

\- Se **o \_ sinalizador WNODE \_ usar o \_ MOF \_ PTR** não for especificado, a carga do evento será construída pelo usuário diretamente na memória, seguindo o [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

O MOF e o WPP são provedores clássicos. No entanto, a implementação de WPP cuida de tudo isso para você.

Para eventos não clássicos, vários [**\_ \_ descritores de dados de evento**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) são passados para [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite). O tempo de execução do ETW concatenará os dados do evento conforme especificado nesses descritores para formar a carga do evento.

As tecnologias baseadas em manifesto e TraceLogging são geralmente provedores modernos. Com base no manifesto, se você permitir que mc.exe gere código de registro para você (comutador um ou km), a geração de carga será levada em volta para você. A geração de carga sempre cuida do TraceLogging.

O resultado final é que uma carga para um evento é gerada em tempo de execução. Todas as cargas são fundamentalmente semelhantes, pois são blobs binários de dados que contêm apenas os dados de campo para esse evento específico, independentemente da tecnologia de rastreamento usada e quais tipos de campo têm suporte nessa tecnologia de rastreamento. Sem os metadados do evento, a carga do evento é inútil e ininteligível.

Em seguida, o imposto do tempo de execução do ETW é para transportar esse blob de eventos do provedor para o consumidor, onde ele é associado novamente a seus metadados e torna-se decodable. O tempo de execução do ETW adicionará um pouco de metadados extras que indicam as circunstâncias da carga, por exemplo, como carimbo de data/hora, ID de thread e palavras-chave do evento. Essas informações são relevantes para o modo como o evento foi roteado por meio do tempo de execução e também é útil para entender a identidade e o contexto do evento ao decodificar o tempo. Ele é eventualmente exibido como parte do rastreamento de [**eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace) ou [**\_ registro de evento**](/windows/win32/api/evntcons/ns-evntcons-event_record) para o consumidor

## <a name="event-metadata"></a>Metadados do evento

A jornada dos metadados de eventos é diferente dependendo de qual tecnologia de rastreamento é usada e é uma das maiores considerações ao comparar cada tecnologia.

### <a name="mof"></a>MOF

Os metadados de evento são criados manualmente pelo criador do evento na forma de um esquema MOF especial em um arquivo. mof. O esquema criado deve corresponder à carga que é registrada para que o evento seja decodificado corretamente pelos consumidores. Os decodificadores de eventos exigem que o arquivo. mof seja registrado no sistema usando [mofcomp.exe](../wmisdk/mofcomp.md). Para obter mais informações sobre como publicar esquemas MOF, consulte [publicando seu esquema de evento para um provedor clássico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>APLICATIVO

Os metadados de evento são gerados automaticamente e armazenados no. pdb de Binary por tracewpp.exe durante o processo de compilação. Esses metadados podem ser extraídos posteriormente na forma de um arquivo. TMF autônomo por meio de tracepdb.exe. Os decodificadores de eventos geralmente exigem o arquivo. pdb ou. TMF. Para obter mais informações sobre tracepdb.exe, consulte [visão geral do Tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview)e para obter mais informações sobre tracewpp.exe, consulte [TraceWPP Task](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Baseado em manifesto

As definições de evento são criadas em um arquivo. Man. Os manifestos de evento são executados por meio do compilador de manifesto ([mc.exe](../wes/message-compiler--mc-exe-.md)), gerando os cabeçalhos necessários para a compilação de origem, bem como vários arquivos de recursos binários. bin. Esses arquivos de recurso devem então ser compilados como recursos em um binário e o binário resultante colocado no sistema que pretende decodificar eventos desse provedor baseado em manifesto. Além disso, o manifesto deve ser instalado no sistema usando [wevtutil.exe](../wes/windows-event-log-tools.md) mais importante, os atributos **resourceFileName** e **messageFileName** no elemento XML do provedor no manifesto do evento instalado devem identificar corretamente o caminho absoluto completo para o binário no qual os arquivos de recurso foram colocados. Observe que esses caminhos podem ser substituídos no horário de instalação do manifesto usando o wevtutil.exe switches/RF e/MF. Um sistema que não tenha sido executado de forma correta e completa essas etapas não conseguirá decodificar eventos desse provedor. Os decodificadores de eventos exigem, portanto, um manifesto instalado e o binário com os recursos associados instalados no local especificado pelos caminhos do arquivo de recursos e mensagens. Para obter mais informações sobre como publicar esquemas baseados em manifesto, consulte [publicando seu esquema de evento para um provedor baseado em manifesto](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Todos os eventos TraceLogging são autodescritivos. Os metadados de evento necessários para decodificar o evento são gerados automaticamente e transmitidos junto com a carga em um formato binário compacto. Os decodificadores de eventos precisam apenas do evento TraceLogging e uma compreensão do formato de metadados TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configurando TDH para decodificação

Há muitas ferramentas de decodificação lá. No entanto, é recomendável que você use TDH sempre que possível, pois ele decodifica todas as tecnologias de rastreamento com uma API unificada. Dependendo do tipo de rastreamento que você está interessado em decodificar, TDH pode exigir configuração explícita.

### <a name="mof"></a>MOF

O TDH utiliza os dados de decodificação do MOF registrados no sistema usando mofcomp.exe. Para obter mais informações, consulte [publicando seu esquema de evento para um provedor clássico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>APLICATIVO

TDH deve ser apontado para o arquivo. pdb ou para o. TMF associado para o provedor WPP que você está tentando decodificar. Isso pode ser executado chamando [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). Caso contrário, o mecanismo de decodificação voltará para o caminho de pesquisa do formato de rastreamento de variável de ambiente \_ \_ \_ .

### <a name="manifest-based"></a>Baseado em manifesto

O TDH utiliza todos os provedores baseados em manifesto registrados no sistema usando wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

As versões mais recentes do TDH detectam e decodificam automaticamente eventos de TraceLogging sem etapas adicionais.

 

 
