---
description: A classe CVideoTransformFilter é projetada principalmente como uma classe base para filtros de descompactador AVI.
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
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826029"
---
# <a name="cvideotransformfilter-class"></a>Classe CVideoTransformFilter

![hierarquia de classe CVideoTransformFilter](images/vtsip01.png)

A `CVideoTransformFilter` classe é projetada principalmente como uma classe base para filtros de descompactador AVI. Essa classe adiciona suporte para controle de qualidade à classe [**CTransformFilter**](ctransformfilter.md) . O método **Receive** do filtro pode decidir descartar quadros, com base em mensagens de qualidade do renderizador e medidas de desempenho que o filtro coleta durante o streaming.

Se o filtro descartar um quadro, ele continuará a descartar os quadros até atingir o próximo quadro-chave. Para fluxos MPEG, o filtro não distingue entre os quadros B e P.



| Variáveis de membro protegido                                                      | Descrição                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**\_bQualityChanged m**](cvideotransformfilter-m-bqualitychanged.md)           | Indica se o filtro removeu quadros.                                               |
| [**\_bSkipping m**](cvideotransformfilter-m-bskipping.md)                       | Indica se o filtro está descartando os quadros no momento.                                     |
| [**\_itrAvgDecode m**](cvideotransformfilter-m-itravgdecode.md)                 | O período médio de tempo necessário para decodificar um quadro.                                         |
| [**\_itrLate m**](cvideotransformfilter-m-itrlate.md)                           | Indica o quanto tarde as amostras chegam ao renderizador.                                   |
| [**\_nFramesSinceKeyFrame m**](cvideotransformfilter-m-nframessincekeyframe.md) | O número de quadros que o filtro recebeu desde o último quadro de chave.                    |
| [**\_nKeyFramePeriod m**](cvideotransformfilter-m-nkeyframeperiod.md)           | O maior intervalo observado entre quadros-chave.                                              |
| [**\_nWaitForKey m**](cvideotransformfilter-m-nwaitforkey.md)                   | O número máximo atual de quadros Delta a serem descartados.                                            |
| [**\_tDecodeStart m**](cvideotransformfilter-m-tdecodestart.md)                 | Período de tempo necessário para decodificar o exemplo mais recente.                                  |
| Métodos Protegidos                                                               | Descrição                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Usado para sinalizar um erro de streaming.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Notifica o filtro de que uma alteração de qualidade é solicitada.                                        |
| [**Recebe**](cvideotransformfilter-receive.md)                                | Recebe um exemplo de mídia, processa-o e entrega um exemplo de saída para o filtro downstream. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Determina se o filtro deve descartar um exemplo especificado.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Chamado quando o filtro alterna para o estado pausado.                                           |
| Métodos públicos                                                                  | Descrição                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Método de construtor.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Finaliza uma operação de liberação.                                                                        |



 

 

 



