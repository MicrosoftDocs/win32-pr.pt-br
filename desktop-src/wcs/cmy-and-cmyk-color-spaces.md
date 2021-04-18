---
title: Espaços de cores CMY e CMYK
description: Os espaços de cores CMY e CMYK geralmente são usados na impressão em cores. Um espaço de cores CMY usa o CMY (ciano, magenta e amarelo) como suas cores primárias. Vermelho, verde e azul são as cores secundárias.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- WCS (sistema de cores do Windows), espaços de cores CMY
- WCS (sistema de cores do Windows), espaços de cores CMY
- gerenciamento de cores de imagem, espaços de cores CMY
- gerenciamento de cores, espaços de cores CMY
- cores, espaços de cores CMY
- espaços de cores, CMY
- Espaços de cores CMY
- WCS (sistema de cores do Windows), espaços de cores CMYK
- WCS (sistema de cores do Windows), espaços de cores CMYK
- gerenciamento de cores de imagem, espaços de cores CMYK
- gerenciamento de cores, espaços CMYKcolors
- cores, espaços de cores CMYK
- espaços de cores, CMYK
- Espaços de cores CMYK
- cyan
- magenta
- yellow
- amarelo magenta ciano (CMY)
- CMY (ciano magenta amarelo)
- preto-magenta amarelo ciano (CMYK)
- CMYK (ciano magenta amarelo preto)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105816058"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Espaços de cores CMY e CMYK

Os [espaços de cores](c.md) CMY e CMYK geralmente são usados na impressão em cores. Um espaço de cores CMY usa o CMY (ciano, magenta e amarelo) como suas [cores primárias](p.md). Vermelho, verde e azul são as cores secundárias.

As figuras a seguir são representações de cor do espaço de cores CMY. O espaço de cores CMY é normalizado.

![cubo de espaço de cores CMY em valores máximos](images/cmyclrs1.png)

![cubo de espaço de cores CMY em valores mínimos](images/cmyclrs2.png)

O espaço de cores CMY é subtraíl. Portanto, o branco está em (0,0, 0,0, 0,0) e o preto está em (1,0, 1,0, 1,0). Se você começar com branco e subtrair sem cores, você terá branco. Se você começar com branco e subtrair todas as cores igualmente, você terá preto.

O espaço de cores CMYK é uma variação no modelo CMY. Ele adiciona preto (ciano, magenta, amarelo e preto). O espaço de cores CMYK fecha a lacuna entre teoria e prática. Teoricamente, o componente preto extra não é necessário. No entanto, a experiência com vários tipos de tintas e documentos mostrou que, quando os componentes iguais de tintas ciano, magenta e amarelo são misturados, o resultado é geralmente um marrom escuro, e não preto. A adição de tinta preta à combinação resolve esse problema.

Os espaços de cores CMY e CMYK podem ser independentes de dispositivo, mas geralmente são usados em referência a um dispositivo específico.

 

 




