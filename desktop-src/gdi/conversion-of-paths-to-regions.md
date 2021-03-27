---
description: Um aplicativo pode converter um caminho em uma região chamando a função PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversão de caminhos em regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661625"
---
# <a name="conversion-of-paths-to-regions"></a>Conversão de caminhos em regiões

Um aplicativo pode converter um caminho em uma região chamando a função [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) . Como [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), o **PathToRegion** é útil na criação de efeitos gráficos especiais. Por exemplo, não há funções que permitam a um aplicativo deslocar um caminho; no entanto, há uma função que permite que um aplicativo offset uma região ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Usando o **PathToRegion** , um aplicativo pode criar o efeito de animar uma forma complexa criando um caminho que define a forma, convertendo o caminho em uma região (chamando **PathToRegion**) e, em seguida, pintando, movendo e apagando a região (chamando funções em uma seqüência, como [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** e **FillRgn**).

 

 



