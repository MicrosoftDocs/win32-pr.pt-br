---
title: Conversão de cores e correspondência de cores
description: O processo de converter cores de um espaço de cor para outro é chamado de conversão de cores.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- WCS (sistema de cores do Windows), conversão de cores
- WCS (sistema de cores do Windows), conversão de cores
- gerenciamento de cores de imagem, conversão de cores
- gerenciamento de cores, conversão de cores
- cores, conversão de cores
- conversão de cores
- WCS (sistema de cores do Windows), correspondência de cores
- WCS (sistema de cores do Windows), correspondência de cores
- gerenciamento de cores de imagem, correspondência de cores
- gerenciamento de cores, correspondência de cores
- cores, correspondência de cores
- correspondência de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- gerenciamento de cores de imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- ponto branco
- colorants
- correção gama
- gama
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105816060"
---
# <a name="color-conversion-and-color-matching"></a>Conversão de cores e correspondência de cores

O processo de converter cores de um [espaço de cor](c.md) para outro é chamado de *conversão de cores*. Todas as cores em um espaço de cores são fixas em relação ao [ponto branco](w.md)do espaço de cores. Como o ponto branco de um espaço de cor varia de dispositivo para dispositivo, uma cor convertida deve ser correspondida à sua cor mais próxima no espaço de cores de destino. Esse processo é chamado de *mapeamento de cores*.

Por exemplo, se você tiver uma imagem digital que você criou na exibição, ela poderá estar em um espaço de cores RGB dependente de dispositivo. Se você quiser imprimi-lo em uma impressora, ele deverá ser convertido no espaço de cores da impressora. Como a impressora provavelmente usa um espaço de cores CMYK dependente de dispositivo, todos os valores RGB devem ser convertidos em CYMK. Esta é a [conversão de cores](c.md). Depois que os valores são especificados em termos do espaço CYMK, eles precisam corresponder à cor mais próxima que a impressora pode produzir. Isso é chamado de mapeamento de cores ou [correspondência de cores](c.md).

A conversão de cores e o mapeamento de cores devem levar em consideração uma série de fatores específicos do dispositivo. Por exemplo, os blocos de construção de imagens de tela são pixels. Cada pixel tem um número definido de bits para armazenar seu valor de índice de cor ou cor. O número de bits por pixel depende do tipo de adaptador de vídeo e exibição que está sendo usado e do modo ao qual o adaptador está definido. A maioria dos tipos de impressora usa diferentes [colorants](c.md) e imprime em resoluções específicas.

Além disso, as características de Tom físico de um dispositivo geralmente são diferentes em dispositivos diferentes. Por exemplo, quando as cores são produzidas por monitores de computador, elas podem parecer diferentes do que se fossem produzidas em uma prensa de impressão. Um fator de correção, chamado de *correção gama*, é frequentemente usado para compensar essas diferenças.

O resultado desses fatores dependentes de dispositivo é que cada dispositivo de cores tem um conjunto específico de cores que ele pode produzir. Esse conjunto de cores é conhecido como sua *gama*. Para executar a conversão de cores e o mapeamento de cores, as cores em uma imagem devem ser convertidas do espaço de cores e da gama do dispositivo de origem no espaço de cores do dispositivo de destino. Em seguida, eles são combinados na gama do dispositivo de destino.

 

 




