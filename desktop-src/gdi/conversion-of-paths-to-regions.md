---
description: Um aplicativo pode converter um caminho em uma região chamando a função PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversão de caminhos em regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d404aa50669fe2349b3e39f172dd652ef765c9de8c615cde446e8540e6051bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062456"
---
# <a name="conversion-of-paths-to-regions"></a>Conversão de caminhos em regiões

Um aplicativo pode converter um caminho em uma região chamando a [**função PathToRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) Assim [**como SelectClipPath,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) **PathToRegion** é útil na criação de efeitos gráficos especiais. Por exemplo, não há nenhuma função que permita que um aplicativo deslocamento um caminho; no entanto, há uma função que permite que um aplicativo deslogue uma região ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Usando **PathToRegion** , um aplicativo pode criar o efeito de animar uma forma complexa criando um caminho que define a forma, convertendo o caminho em uma região (chamando **PathToRegion**) e, em seguida, pintando repetidamente, movendo e apagando a região (chamando funções em uma sequência, como [**FillRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) **OffsetRgn** e **FillRgn**).

 

 



