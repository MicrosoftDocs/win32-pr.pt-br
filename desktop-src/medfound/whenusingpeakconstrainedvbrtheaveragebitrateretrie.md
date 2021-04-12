---
description: Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico. Como isso é possível?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296617"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Quando uso a VBR com restrição de pico, a taxa média de bits recuperada do objeto codec é maior do que a taxa de bits de pico. Como isso é possível?

A relação entre a taxa média de bits e a taxa de bits de pico geralmente é mal compreendida. A taxa de bits de pico descreve uma restrição de buffer ao longo de um período de tempo especificado pela janela de pico do buffer. A taxa média de bits para a VBR de duas passagens (irrestrito ou com restrição de pico) é a média de bits por segundo durante a duração do arquivo.

Conforme descrito no [modelo de buffer de Bucket vazado](the-leaky-bucket-buffer-model.md), a taxa de bits real usada em um período de tempo igual à janela de buffer pode aproximar duas vezes a taxa de bits. Isso ocorre porque o buffer, definido como um número de bits igual à taxa de bits, o tempo da janela de buffer (em segundos), está sendo esvaziado a uma taxa constante.

Por exemplo, em um segundo de um fluxo de 56 Kbps, o codificador cria amostras que totalizam 59 KB. Portanto, 56 KB de dados é removido do buffer nesse segundo, deixando 3 KB no buffer. Se o fluxo tiver uma janela de buffer de três segundos e, portanto, um tamanho de buffer total de 168 KB, levaria quase 40 segundos para preencher o buffer. A taxa média de bits para o fluxo (se sua duração for menor do que o tempo necessário para preencher o buffer) for de 59 Kbps, mesmo que a taxa de bits seja definida como 56 Kbps.

O mesmo fenômeno se aplica a restrições de taxa de bits de pico. Para conteúdo curto, a taxa média de bits computada pelo objeto codec após a codificação ser concluída pode ser maior que a taxa de bits de pico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



