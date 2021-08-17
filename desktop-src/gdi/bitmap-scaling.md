---
description: A função StretchBlt dimensiona um bitmap executando uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem em um retângulo em um contexto de dispositivo de destino.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Dimensionamento de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14975f884906fb95bf07fbf3ab5277b89c5cbfd2612864202eb64eedc5df646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699893"
---
# <a name="bitmap-scaling"></a>Dimensionamento de bitmap

A função [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) dimensiona um bitmap executando uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem em um retângulo em um contexto de dispositivo de destino. No entanto, ao contrário da função [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , que duplica as dimensões do retângulo de origem no retângulo de destino, o **StretchBlt** permite que um aplicativo especifique as dimensões dos retângulos de origem e de destino. Quando o bitmap de destino é menor do que o bitmap de origem, o sistema combina linhas ou colunas de dados de cor (ou ambos) no bitmap antes de renderizar a imagem correspondente no dispositivo de vídeo. O sistema combina os dados de cor de acordo com o modo de ampliação especificado, que o aplicativo define chamando a função [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) . Quando o bitmap de destino é maior do que o bitmap de origem, o sistema dimensiona ou amplia cada pixel na imagem resultante de acordo.

 

 



