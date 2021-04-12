---
title: Arquivo enviado por push
description: Arquivo enviado por push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos enviados por push
- Capas móveis do Windows Media Player, arquivos enviados por push
- capas, arquivos enviados por push
- Arquivos enviados por push em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364083"
---
# <a name="pushed-file"></a>Arquivo enviado por push

O arquivo enviado contém as imagens que serão exibidas quando o usuário tocar em um botão. Você também pode incluir as imagens normal e push para o estado de pausa do botão PlayPause.

A imagem a seguir é um arquivo Push típico.

![arquivo enviado por push](images/cesdkpus.png)

Isso armazena as imagens que serão exibidas quando os botões de tipo de clique forem tocados. Também armazenados nesse arquivo são as imagens normais e enviadas por push para a imagem pausada do botão PlayPause. Exceto pelas imagens secundárias PlayPause à direita, as outras imagens de botão são alinhadas com a imagem de plano de fundo, usando o deslocamento definido na seção bitmaps do arquivo de definição de capa.

Observe que o plano de fundo da imagem do botão corresponde exatamente à área correspondente no arquivo de plano de fundo. Isso é importante, porque quando o usuário toca em um botão de tipo de ocorrência, o retângulo inteiro definido para a imagem enviada por push substituirá a área correspondente no arquivo em segundo plano. Mantenha o gráfico consistente com a imagem de plano de fundo para garantir que apenas as partes do botão que você deseja que sejam diferentes sejam alteradas de fato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




