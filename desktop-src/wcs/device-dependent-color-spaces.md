---
title: Espaços de cores dependentes do dispositivo
description: A maioria dos espaços de cores são dependentes do dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- WCS (sistema de cores do Windows), espaços de cores dependentes do dispositivo
- WCS (sistema de cores do Windows), espaços de cores dependentes do dispositivo
- gerenciamento de cores de imagem, espaços de cores dependentes do dispositivo
- gerenciamento de cores, espaços de cores dependentes do dispositivo
- cores, espaços de cores dependentes do dispositivo
- espaços de cores, dependentes do dispositivo
- espaços de cores dependentes do dispositivo
- ponto branco
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105769669"
---
# <a name="device-dependent-color-spaces"></a>Espaços de cores dependentes do dispositivo

A maioria dos [espaços de cores](c.md) são dependentes do dispositivo. Embora um dispositivo específico, como uma impressora, possa usar o espaço de cores CMYK, as cores que ele renderiza para valores CMYK específicos geralmente são um pouco diferentes de todos os outros tipos de impressoras. É precisamente por esse motivo que o sistema de gerenciamento de cores WCS 1,0 é tão útil.

Todos os espaços de cores têm um *ponto branco*, que é definido como o branco mais branco que pode ser produzido nesse espaço de cores. Como os dispositivos podem diferir um do outro, seus pontos brancos também podem diferir. Todas as cores que um dispositivo pode produzir são relativas a seu ponto branco. Portanto, um sistema de gerenciamento de cores deve ser capaz de mapear o ponto branco de um espaço de cor para outro e preservar os locais relativos de todas as cores. Ele também deve ser capaz de mapear uma cor em um espaço de cor para sua correspondência mais próxima em outro espaço de cores, independentemente das diferenças nos pontos brancos. O WCS 1,0 é capaz de realizar essas duas tarefas.

O espaço de cores RGB geralmente é usado em monitores de computador. Como tal, é dependente de dispositivo. As impressoras normalmente usam [COLORANTS](c.md)CMYK. Cada impressora implementa sua própria versão do espaço de cores CMYK. As imagens digitais podem, na verdade, armazenar as cores nelas. Eles podem armazenar números de índice em uma paleta de cores. O resultado é que é muito difícil para os desenvolvedores de aplicativos individuais usarem ou fornecerem um método padronizado de movimentação de imagens coloridas de um dispositivo para outro. Os profissionais de geração de imagens normalmente experimentam a frustração de criar uma imagem gráfica em uma tela de computador e fazer com que ela se transforme de maneira muito diferente quando impressa. O WCS 1,0 aborda essas necessidades de geração de imagens.

 

 




