---
title: Super arquivos
description: Super arquivos
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Capas móveis, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos Super files
- Windows Media Player Capas móveis, arquivos Super
- skins, Super files
- Super arquivos em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbd6734e0491b5fc0e6552db14b3c0ab4489e466e7851ef4b474e84d2d85183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122856"
---
# <a name="super-files"></a>Super arquivos

Os superarmadores são usados para armazenar as imagens desabilitadas para barras de faixa. Como a imagem principal da barra de faixas é exibida no arquivo Background e o usuário toca na imagem do thumb, não na imagem da barra de faixas, somente a imagem Desabilitada é necessária para barras de faixa. Ele é armazenado no arquivo definido por Super na seção Bitmaps do arquivo de definição de capa. Um arquivo Super também pode armazenar as imagens Enviada por Pushed e Disabled para outros botões, como Mute, que não é necessário para ser um botão de tipo de clique.

> [!Note]  
> Os arquivos de super-arte não são usados em capas do Windows Media Player 10 Mobile ou posterior porque as imagens desabilitadas para barras de faixa de busca estão localizadas no arquivo seekthumb.

 

A imagem a seguir é um arquivo Super típico.

![superar arquivo](images/cesdksup.png)

Isso armazena as imagens desabilitadas para as barras de faixa e o botão de mudo. Essas imagens são deslocadas conforme definido pela seção Bitmaps.

A área de fundo da imagem da barra de faixa desabilitada corresponde exatamente à área correspondente no arquivo Background. Isso é importante, porque todo o retângulo definido para a imagem da barra de faixa desabilitada substituirá a área correspondente no arquivo Background. Isso garante que a imagem da barra de faixa desabilitada se combina perfeitamente com a imagem de plano de fundo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




