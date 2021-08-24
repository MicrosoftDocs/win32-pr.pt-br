---
title: Espaços de cores CMY e CMYK
description: Os espaços de cores CMY e CMYK geralmente são usados na impressão de cores. Um espaço de cores CMY usa ciano, magenta e amarelo (CMY) como suas cores primárias. Vermelho, verde e azul são as cores secundárias.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Sistema de Cores (WCS), espaços de cores CMY
- WCS (Windows color system), espaços de cores CMY
- gerenciamento de cores da imagem, espaços de cores do CMY
- gerenciamento de cores, espaços de cores do CMY
- cores, espaços de cores CMY
- espaços de cores, CMY
- Espaços de cores CMY
- Windows WCS (Sistema de Cores), espaços de cores do CMYK
- WCS (Windows color system), espaços de cores do CMYK
- gerenciamento de cores da imagem, espaços de cores do CMYK
- gerenciamento de cores, espaços CMYKcolor
- cores, espaços de cores do CMYK
- espaços de cores, CMYK
- Espaços de cores do CMYK
- cyan
- magenta
- yellow
- Ciano yellow (CMY)
- CMY (amarelo ciano magenta)
- Cyan magenta yellow black (CMYK)
- CMYK (preto amarelo em ciano)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcb1ea33bd32346dd541894342ec4af02274e4381eaf0c1925e2a4bc20e10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452087"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Espaços de cores CMY e CMYK

Os espaços de cores CMY [e](c.md) CMYK geralmente são usados na impressão de cores. Um espaço de cores CMY usa ciano, magenta e amarelo (CMY) como suas [cores primárias.](p.md) Vermelho, verde e azul são as cores secundárias.

As figuras a seguir são representações de cores do espaço de cores CMY. O espaço de cores do CMY é normalizado.

![cmy color space cube em valores máximos](images/cmyclrs1.png)

![cmy color space cube com valores mínimos](images/cmyclrs2.png)

O espaço de cores do CMY é subtrativo. Portanto, branco está em (0,0, 0,0, 0,0) e preto está em (1.0, 1.0, 1.0). Se você começar com branco e não subtrair nenhuma cor, obterá branco. Se você começar com branco e subtrair todas as cores igualmente, você obterá preto.

O espaço de cores do CMYK é uma variação no modelo CMY. Ele adiciona preto (Ciano, Magenta, Amarelo e blacK). O espaço de cores do CMYK fecha a lacuna entre a teoria e a prática. Em teoria, o componente preto extra não é necessário. No entanto, a experiência com vários tipos de tintas e documentos mostrou que, quando componentes iguais de tintas ciano, magenta e amarelo são mistos, o resultado geralmente é um marrom escuro, não preto. Adicionar tinta preta à combinação resolve esse problema.

Os espaços de cores CMY e CMYK podem ser independentes do dispositivo, mas geralmente são usados em referência a um dispositivo específico.

 

 




