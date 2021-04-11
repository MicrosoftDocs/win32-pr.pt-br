---
description: Configurando os Pins de saída do Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configurando os Pins de saída do Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087723"
---
# <a name="configuring-the-demux-output-pins"></a>Configurando os Pins de saída do Demux

Quando o Demux MPEG-2 recebe um pacote de dados, ele deve determinar qual pino de saída deve analisar e entregar os dados. No modo de fluxo do programa, o Demux mapeia as IDs de fluxo para os Pins de saída. No modo de fluxo de transporte, ele mapeia PIDs para Pins de saída. Por exemplo, no modo de fluxo de transporte, se PID 0x31 for mapeado para o pino 0, todos os pacotes TS com esse número PID serão roteados para o pino de saída 0. Se o Demux receber um pacote cuja ID de fluxo ou PID não esteja mapeado para nenhum pino de saída, ele simplesmente descartará o pacote.

No modo de pull, o Demux cria automaticamente os Pins de saída para os fluxos de áudio e vídeo no arquivo e mapeia as IDs de fluxo para os Pins.

No modo de push, os Pins de saída devem ser configurados pelo aplicativo ou por outro filtro. Para fontes de televisão digital que usam a arquitetura de driver de difusão (BDA), o filtro do provedor de rede funciona com o filtro TIF para configurar o Demux. O aplicativo não precisa fazer nada. Em outros cenários, o aplicativo deve configurar os Pins de saída.

O Demux começa sem nenhum pino de saída. Para criar um PIN de saída, chame o método [**IMpeg2Demultiplexer:: CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) no filtro. Esse método usa um tipo de mídia e um nome de PIN e retorna um ponteiro **IPin** . O tipo de mídia é usado quando o PIN se conecta a outro filtro, normalmente um decodificador — um exemplo recebe a seção [usando o demux com fluxos elementares](using-the-demux-with-elementary-streams.md). O nome do PIN pode ser qualquer coisa que você desejar, exceto que nomes de PIN duplicados não são permitidos.

Em seguida, atribua um ou mais IDs de fluxo ou PIDs ao novo pino de saída. Para fluxos de programa, consulte o PIN para **IMPEG2StreamIdMap** e chame [**IMPEG2StreamIdMap:: MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Para fluxos de transporte, consulte o PIN para **IMPEG2PIDMap** e chame [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Há várias maneiras pelas quais o Demux pode analisar pacotes TS. Para cada pino de saída, o método de análise é determinado pelo parâmetro *MediaSampleContent* para o método **MapPID** .



| Valor                     | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fluxo elementar mídia \_ | O filtro fornece cargas de PES. Nesse modo, o filtro depacketizes os pacotes PES, de modo que o filtro downstream recebe o fluxo de ES, sem os cabeçalhos de pacote PES. (Somente fluxos de áudio e vídeo.)                                                                                                                                                     |
| MPEG2 de mídia \_ \_ psi         | O filtro fornece as seções PSI completas, como as tabelas PAT, as tabelas PGTO, as tabelas CAT e assim por diante.                                                                                                                                                                                                                                                               |
| \_carga de transporte de mídia \_ | O filtro extrai as cargas dos pacotes TS e as entrega sem análise adicional. Para fluxos elementares, isso significa que o Demux fornecerá pacotes PES inteiros, incluindo os cabeçalhos de pacote PES.                                                                                                                                                    |
| \_pacote de transporte de mídia \_  | O filtro fornece pacotes TS inteiros. O Demux roteia os pacotes TS de acordo com seus PIDs, mas não examina nem processa os pacotes. Os pacotes com erros não são filtrados. O Demux não remultiplexa os pacotes e o fluxo de saída resultante não é um fluxo de transporte MPEG-2 em conformidade. Esse modo é chamado de modo de *passagem* . |



 

Para fluxos de programa, o Demux sempre entrega cargas PES.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



