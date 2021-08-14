---
title: Arquivo pressionado
description: Arquivo pressionado
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Windows Media Player Capas móveis, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos pressionados
- Windows Media Player Capas móveis, arquivos pressionados
- capas, arquivos pressionados
- Arquivos pressionados em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0526cad560abfbee3a7ec6cbaa0c355a51d93c2080d7c1ef933f7caaf867ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570667"
---
# <a name="pushed-file"></a>Arquivo pressionado

O arquivo por pushed contém as imagens que serão exibidas quando o usuário tocar em um botão. Você também pode incluir as imagens normais e pressionadas para o estado de pausa do botão PlayPause.

A imagem a seguir é um arquivo típico por pushed.

![arquivo pressionado](images/cesdkpus.png)

Isso armazena as imagens que serão exibidas quando os botões de tipo de clique são mapeados. Também são armazenadas nesse arquivo as imagens normais e enviada por pushed para a imagem em pausa do botão PlayPause. Com exceção das imagens secundárias do PlayPause à direita, as outras imagens de botão são alinhadas com a imagem De plano de fundo, usando o deslocamento definido na seção Bitmaps do arquivo de definição de capa.

Observe que a plano de fundo da imagem do botão corresponde exatamente à área correspondente no arquivo Background. Isso é importante, porque quando o usuário toca em um botão de tipo de clique, todo o retângulo definido para a imagem pressionada substituirá a área correspondente no arquivo Background. Mantenha o gráfico consistente com a imagem de plano de fundo para garantir que apenas as partes do botão que você deseja que apareçam diferentes realmente serão mudadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




