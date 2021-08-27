---
title: Conversão de cores e correspondência de cores
description: O processo de conversão de cores de um espaço de cores em outro é chamado de conversão de cores.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Sistema de Cores (WCS), conversão de cores
- WCS (Windows color system),conversão de cores
- gerenciamento de cores da imagem, conversão de cores
- gerenciamento de cores, conversão de cores
- cores, conversão de cores
- conversão de cores
- Windows Sistema de Cores (WCS), correspondência de cores
- WCS (Windows color system), correspondência de cores
- gerenciamento de cores da imagem, correspondência de cores
- gerenciamento de cores, correspondência de cores
- cores, correspondência de cores
- correspondência de cores
- Windows Sistema de Cores (WCS), mapeamento de cores
- WCS (Windows color system),mapeamento de cores
- gerenciamento de cores da imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- ponto branco
- Corantes
- correção gama
- Gama
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0071e15c2d572c134d61aee7a018b41c8d09507e87963eeeed1488909cdafeba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110796"
---
# <a name="color-conversion-and-color-matching"></a>Conversão de cores e correspondência de cores

O processo de conversão de cores de um [espaço de cor](c.md) para outro é chamado de *conversão de cores*. Todas as cores em um espaço de cores são fixas em relação ao ponto branco [do espaço de cores.](w.md) Como o ponto branco de um espaço de cor varia de dispositivo para dispositivo, uma cor convertida deve ser então corresponder à cor visualmente mais próxima no espaço de cores de destino. Esse processo é chamado de *mapeamento de cores.*

Por exemplo, se você tiver uma imagem digital criada na exibição, ela poderá estar em um espaço de cores RGB dependente do dispositivo. Se você quiser imprimi-lo em uma impressora, ele deverá ser convertido no espaço de cores da impressora. Como a impressora provavelmente usa um espaço de cor CMYK dependente do dispositivo, todos os valores RGB devem ser convertidos em CYMK. Essa é a [conversão de cores](c.md). Depois que os valores são especificados em termos de espaço CYMK, eles precisam ser corresponder à cor mais próxima que a impressora pode produzir. Isso é chamado de mapeamento de cores ou [correspondência de cores.](c.md)

A conversão de cores e o mapeamento de cores devem levar em conta vários fatores específicos do dispositivo. Por exemplo, os blocos de construção de imagens de tela são pixels. Cada pixel tem um número definido de bits para armazenar seu valor de índice de cor ou cor. O número de bits por pixel depende do tipo de adaptador de exibição e exibição que está sendo usado e do modo para o qual o adaptador está definido. A maioria dos tipos de impressora usa [colorantes diferentes](c.md) e imprime em resoluções específicas.

Além disso, as características de tom físico de um dispositivo geralmente são diferentes em dispositivos diferentes. Por exemplo, quando as cores são produzidas por monitores de computador, elas podem aparecer diferentes do que seriam se fossem produzidas em uma impressora. Um fator de correção, chamado *correção gama,* é frequentemente usado para compensar essas diferenças.

O resultado desses fatores dependentes do dispositivo é que cada dispositivo de cor tem um conjunto específico de cores que ele pode produzir. Esse conjunto de cores é conhecido como *seu gamut*. Para executar a conversão de cores e o mapeamento de cores, as cores em uma imagem devem ser convertidas do espaço de cores e da gama do dispositivo de origem no espaço de cores do dispositivo de destino. Em seguida, eles são corresponderes ao gamut do dispositivo de destino.

 

 




