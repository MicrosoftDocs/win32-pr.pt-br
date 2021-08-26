---
description: Definindo propriedades de captura de áudio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Definindo propriedades de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078806"
---
# <a name="setting-audio-capture-properties"></a>Definindo propriedades de captura de áudio

Cada pino de entrada no filtro de captura de áudio expõe a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) . Use essa interface para habilitar ou desabilitar uma entrada específica, chamando o método [**IAMAudioInputMixer::p UT \_ Enable**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) no PIN. Além disso, use essa interface para definir as propriedades de uma entrada, como os níveis de baixo, agudos e volume. Se você estiver capturando várias entradas de uma só vez, poderá controlar os níveis gerais de baixo, agudo e volume por meio da interface **IAMAudioInputMixer** no próprio filtro.

As taxas de amostragem e os formatos de áudio disponíveis para captura são determinados pelo driver. Use a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) no pino de saída do filtro de captura de áudio para enumerar as taxas e os formatos de amostragem disponíveis e defina o formato desejado. O filtro pode conectar downstream a qualquer filtro que aceite o tipo de mídia do pino de saída.

O filtro de captura de áudio também expõe a interface [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) . Essa interface é útil para controlar a quantidade de latência na visualização de áudio. Por padrão, o filtro de captura de áudio usa um tamanho de buffer de meio segundo. Esse tamanho de buffer é ideal para a captura, mas causa um atraso de visualização de meio segundo. Para reduzir a latência, chame o método [**IAMBufferNegotiation:: SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) antes de conectar o pino de saída do filtro de captura de áudio. Esse método usa um ponteiro para a estrutura de [**\_ Propriedades do alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) . Use o membro **cbBuffer** para especificar o tamanho do buffer, em bytes. Um buffer de 80 milissegundos é geralmente seguro, mas buffers de 30 ou 40 milissegundos podem ser suficientes. Se os buffers forem muito pequenos, a qualidade do som será degradada.

 

 



