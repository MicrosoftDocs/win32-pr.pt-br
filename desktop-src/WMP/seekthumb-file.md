---
title: Arquivo SeekThumb
description: Arquivo SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos SeekThumbd
- Capas móveis do Windows Media Player, arquivos SeekThumb
- capas, arquivos SeekThumb
- Arquivos SeekThumb em capas
- Thumb, arquivos SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916406"
---
# <a name="seekthumb-file"></a>Arquivo SeekThumb

O arquivo SeekThumb define a imagem que indica o local de reprodução dentro do item de mídia para um TrackBar de busca. Você pode usar um arquivo e defini-lo para uso por SeekThumb e VolumeThumb. Ao contrário dos outros arquivos de arte, os arquivos Thumb são definidos na seção trackbars do arquivo de definição de capa.

A imagem a seguir é um arquivo SeekThumb típico.

![arquivo seekthumb](images/cesdksee.gif)

Esses dois arquivos de botão têm a mesma aparência, mas são tamanhos um pouco diferentes. A imagem esquerda é a exibição normal que o usuário vê e a imagem correta é a imagem enviada pelo usuário quando toca no botão.

> [!Note]  
> Arquivos de arte SeekThumb criados para capas usadas no Windows Media Player 10 Mobile ou posterior devem ter as três imagens a seguir (da esquerda para a direita): normal, enviada por push e desabilitado.

 

Talvez você queira tornar as áreas de imagens de polegar transparentes. Isso permitirá que você crie imagens thumbs em formas diferentes de retangulares. Qualquer região de uma imagem Thumb que você preenche com a cor especificada pelo valor RGB 255, 0, 255 aparecerá transparente em sua capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




