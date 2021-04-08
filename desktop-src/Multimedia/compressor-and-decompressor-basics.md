---
title: Noções básicas de compressor e descompactador
description: Noções básicas de compressor e descompactador
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- VCM (Gerenciador de compactação de vídeo), abrindo compactadores
- VCM (Gerenciador de compactação de vídeo), abrindo compactadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822586"
---
# <a name="compressor-and-decompressor-basics"></a>Noções básicas de compressor e descompactador

Para abrir e localizar um compressor, você pode usar as funções [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Você pode usar o **ICLocate** para encontrar um compressor de um tipo específico e obter um identificador de ti para uso em outras funções do VCM. Para abrir um compressor, você pode usar **ICOpen**. Seu aplicativo usa o identificador retornado por essa função para identificar o compactador aberto quando ele usa outras funções VCM.

Para abrir e localizar um descompactador, os aplicativos podem usar as macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) . Essas macros usam **ICLocate** para a operação.

Quando o aplicativo tiver terminado de usar um compactador ou descompactador, ele deverá fechá-lo para liberar todos os recursos usados para compactação ou descompactação. Seu aplicativo pode usar a função [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para fechar o compressor ou o descompactador.

Além disso, seu aplicativo pode enumerar os compactadores ou os decompactadores em um sistema usando a função [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .

> [!Note]  
> O cabeçalho de fluxo em um arquivo AVI contém informações sobre o tipo de fluxo e o manipulador específico para esse fluxo. Dentro do cabeçalho do fluxo, os membros **fccType** e **fccHandler** identificam o tipo de fluxo e o manipulador de fluxo especificado para o fluxo.

 

 

 




