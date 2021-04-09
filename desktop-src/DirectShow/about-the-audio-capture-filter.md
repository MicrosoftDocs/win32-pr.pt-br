---
description: Sobre o filtro de captura de áudio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Sobre o filtro de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087859"
---
# <a name="about-the-audio-capture-filter"></a>Sobre o filtro de captura de áudio

O DirectShow habilita a captura de entradas analógicas em uma placa de som por meio do [filtro de captura de áudio](audio-capture-filter.md). Esse filtro usa as APIs do wavee *xxx* para controlar qualquer dispositivo cujo driver dê suporte a essas APIs. Cada cartão no sistema é representado por uma instância separada do filtro.

O filtro de captura de áudio expõe cada entrada no cartão, como o microfone ou a entrada MIDI, como um pino de entrada. Os Pins de entrada representam o que o driver expõe como linhas de origem de áudio. No entanto, nenhum dado passa por esses Pins de entrada e eles não se conectam a outros filtros do DirectShow. Eles simplesmente fornecem uma maneira para um aplicativo controlar as entradas. O aplicativo pode usar um PIN de entrada para habilitar ou desabilitar a entrada, ou para definir propriedades de combinação como equalização Bass, equalização de agudo, panorâmica e assim por diante. A quantidade de controle disponível depende do driver. Para compreender e explorar totalmente os recursos de uma placa de som específica, você precisará da documentação do fabricante do cartão.

> [!Note]  
> Você pode capturar da entrada de CD-Audio, mas esse fluxo de áudio já passou pelo conversor digital para analógico, portanto, haverá uma perda de qualidade de som do CD original.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 



