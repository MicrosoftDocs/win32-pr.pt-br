---
description: Configurando os pinos de saída do Demux
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Configurando os pinos de saída do Demux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0456b7354c23048bafe012439d5d2c4fa1843df601ee2d8e49aa62dfc01a4b9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813606"
---
# <a name="configuring-the-demux-output-pins"></a>Configurando os pinos de saída do Demux

Quando o demux MPEG-2 recebe um pacote de dados, ele deve determinar qual pino de saída deve analisar e entregar os dados. No modo de fluxo do programa, o demux mapeia IDs de fluxo para pinos de saída. No modo de fluxo de transporte, ele mapeia PIDs para pinos de saída. Por exemplo, no modo de fluxo de transporte, se o PID 0x31 for mapeado para fixar 0, cada pacote TS com esse número PID será roteado para o pino de saída 0. Se o demux receber um pacote cuja ID de fluxo ou PID não está mapeada para qualquer pino de saída, ele simplesmente descarta o pacote.

No modo de pull, o demux cria automaticamente pinos de saída para os fluxos de áudio e vídeo no arquivo e mapeia as IDs de fluxo para os pinos.

No modo de push, os pinos de saída devem ser configurados pelo aplicativo ou por outro filtro. Para fontes de tv digital usando a BDA (Arquitetura de Driver de Difusão), o filtro do provedor de rede funciona com o filtro TIF para configurar o demux. O aplicativo não precisa fazer nada. Em outros cenários, o aplicativo deve configurar os pinos de saída.

O demux começa sem pinos de saída. Para criar um pin de saída, chame o [**método IMpeg2Demultiplexer::CreateOutputPin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) no filtro. Esse método aceita um tipo de mídia e um nome de pino e retorna um **ponteiro IPin.** O tipo de mídia é usado quando o pino se conecta a outro filtro, normalmente um decodificador – um exemplo recebe a seção Usando o [Demux](using-the-demux-with-elementary-streams.md)com o Fluxos . O nome do pino pode ser qualquer coisa que você quiser, exceto que nomes de pino duplicados não são permitidos.

Em seguida, atribua uma ou mais IDs de fluxo ou PIDs ao novo pino de saída. Para fluxos de programas, consulte o pin para **IMPEG2StreamIdMap** e chame [**IMPEG2StreamIdMap::MapStreamId**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Para fluxos de transporte, consulte o pino para **IMPEG2PIDMap** e chame [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Há várias maneiras pelas quais o demux pode analisar pacotes TS. Para cada pino de saída, o método de análise é determinado pelo *parâmetro MediaSampleContent* para o **método MapPID.**



| Valor                     | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLUXO \_ ELEMENTAR DE \_ MÍDIA | O filtro fornece cargas PES. Nesse modo, o filtro desempacota os pacotes pes, de modo que o filtro downstream recebe o fluxo de byte do ES, sem os headers de pacote pes. (Somente fluxos de áudio e vídeo.)                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | O filtro fornece seções PSI completas, como tabelas PAT, tabelas PMT, tabelas CAT e assim por diante.                                                                                                                                                                                                                                                               |
| CARGA DE \_ TRANSPORTE \_ DE MÍDIA | O filtro extrai os conteúdos dos pacotes TS e os entrega sem análise posterior. Para fluxos elementares, isso significa que o demux fornecerá pacotes pes inteiros, incluindo os headers de pacotes pes.                                                                                                                                                    |
| PACOTE DE \_ TRANSPORTE \_ DE MÍDIA  | O filtro fornece pacotes TS inteiros. O demux encaminha os pacotes TS de acordo com seus PIDs, mas não examina ou processa os pacotes de outra forma. Pacotes com erros não são filtrados. O demux não multiplexa os pacotes e o fluxo de saída resultante não é um fluxo de transporte MPEG-2 compatível. Esse modo é chamado *de modo de* passagem. |



 

Para fluxos de programas, o demux sempre fornece cargas de PES.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Demultiplexer MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



