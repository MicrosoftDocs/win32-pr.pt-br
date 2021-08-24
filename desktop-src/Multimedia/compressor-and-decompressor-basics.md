---
title: Noções básicas sobre o Descompactador e o Descompactador
description: Noções básicas sobre o Descompactador e o Descompactador
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- VCM (gerenciador de compactação de vídeo), abrindo os vcms
- VCM (gerenciador de compactação de vídeo), abrindo os vcms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1969748949aeb023f889bc651ccd028f19c3e18fe6cf1ba088b4f4ec29292f35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144989"
---
# <a name="compressor-and-decompressor-basics"></a>Noções básicas sobre o Descompactador e o Descompactador

Para abrir e localizar um , você pode usar as [**funções ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen.**](/windows/desktop/api/Vfw/nf-vfw-icopen) Você pode usar **ICLocate** para localizar um grupo de um tipo específico e obter um identificador dele para uso em outras funções vcm. Para abrir um , você pode usar **ICOpen**. Seu aplicativo usa o identificador retornado por essa função para identificar o ao usar outras funções VCM abertas.

Para abrir e localizar um descompactador, os aplicativos podem usar as macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen.**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) Essas macros usam **ICLocate para** operação.

Quando o aplicativo terminar de usar um descompactador ou um descompactador, ele deverá ser fechado para liberar todos os recursos usados para compactação ou descompactação. Seu aplicativo pode usar a [**função ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para fechar o minicompactador ou o descompactador.

Além disso, seu aplicativo pode enumerar os descompactores ou os descompactores em um sistema usando a [**função ICInfo.**](/windows/desktop/api/Vfw/nf-vfw-icinfo)

> [!Note]  
> O header de fluxo em um arquivo AVI contém informações sobre o tipo de fluxo e o manipulador específico para esse fluxo. Dentro do header de fluxo, os **membros de digitType** **ehandler** identificam o tipo de fluxo e o manipulador de fluxo especificado para o fluxo.

 

 

 




