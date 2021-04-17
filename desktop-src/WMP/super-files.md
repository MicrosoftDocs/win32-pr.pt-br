---
title: Super arquivos
description: Super arquivos
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos de Super arquivos
- Capas móveis do Windows Media Player, arquivos de superarquivos
- capas, Super arquivos
- Super arquivos em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105812232"
---
# <a name="super-files"></a>Super arquivos

Super arquivos são usados para armazenar as imagens desabilitadas para trackbars. Como a imagem principal do TrackBar é exibida no arquivo em segundo plano e o usuário toca na imagem do Thumb, não na imagem do TrackBar, apenas a imagem desabilitada é necessária para trackbars. Ele é armazenado no arquivo definido por super na seção bitmaps do arquivo de definição de capa. Um superarquivo também pode armazenar as imagens enviadas e desativadas para outros botões, como mudo, o que não é necessário para um botão de tipo de clique.

> [!Note]  
> Arquivos de superarte não são usados em capas para o Windows Media Player 10 Mobile ou posterior porque as imagens desabilitadas para o trackbars de busca estão localizadas no arquivo seekthumb.

 

A imagem a seguir é um super arquivo típico.

![Super arquivo](images/cesdksup.png)

Isso armazena as imagens desabilitadas para o trackbars e o botão mudo. Essas imagens são deslocadas conforme definido pela seção bitmaps.

A área de plano de fundo da imagem TrackBar desabilitada corresponde exatamente à área correspondente no arquivo de plano de fundo. Isso é importante, pois o retângulo inteiro definido para a imagem TrackBar desabilitada substituirá a área correspondente no arquivo de plano de fundo. Isso garante que a imagem TrackBar desabilitada se misture diretamente na imagem de plano de fundo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




