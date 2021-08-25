---
description: A classe CVideoTransformFilter foi projetada principalmente como uma classe base para filtros de descompactador AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Classe CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: a1e1a1b717aeb2814b469fc34a9e038052abb6720dde0ed75982f27716978de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906997"
---
# <a name="cvideotransformfilter-class"></a>Classe CVideoTransformFilter

![Hierarquia de classes cvideotransformfilter](images/vtsip01.png)

A `CVideoTransformFilter` classe foi projetada principalmente como uma classe base para filtros de descompactador AVI. Essa classe adiciona suporte para controle de qualidade à [**classe CTransformFilter.**](ctransformfilter.md) O método **Receive** do filtro pode decidir soltar quadros, com base nas mensagens de qualidade do renderdor e nas medidas de desempenho que o filtro coleta enquanto está transmitindo.

Se o filtro descarta um quadro, ele continua a soltar quadros até atingir o próximo quadro-chave. Para fluxos MPEG, o filtro não faz distinção entre quadros B e quadros P.



| Variáveis de membro protegidas                                                      | Descrição                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Indica se o filtro baixou quadros.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Indica se o filtro está soltando quadros no momento.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Tempo médio que levou para decodificar um quadro.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Indica a hora em que os exemplos estão chegando ao renderador.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | O número de quadros que o filtro recebeu desde o último quadro-chave.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | O maior intervalo observado entre quadros-chave.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | O número máximo atual de quadros delta a ser baixado.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Tempo necessário para decodificar a amostra mais recente.                                  |
| Métodos Protegidos                                                               | Descrição                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Usado para sinalizar um erro de streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica o filtro de que uma alteração de qualidade é solicitada.                                        |
| [**Receber**](cvideotransformfilter-receive.md)                                | Recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina se o filtro deve soltar um exemplo especificado.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Chamado quando o filtro alterna para o estado em pausa.                                           |
| Métodos públicos                                                                  | Descrição                                                                                    |
| [**Cvideotransformfilter**](cvideotransformfilter-cvideotransformfilter.md)    | Método do construtor.                                                                            |
| [**Endflush**](cvideotransformfilter-endflush.md)                              | Encerra uma operação de liberação.                                                                        |



 

 

 



