---
title: Arquivo desabilitado
description: Arquivo desabilitado
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos desabilitados
- Capas móveis do Windows Media Player, arquivos desabilitados
- capas, arquivos desabilitados
- Arquivos desabilitados em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005768"
---
# <a name="disabled-file"></a>Arquivo desabilitado

O arquivo desabilitado contém as imagens que serão exibidas quando uma função de botão específica não puder ser usada ou se um estado de botão estiver desativado. Por exemplo, se uma lista de reprodução vazia for definida, os botões **Avançar** e **anterior** serão exibidos e deverão ser exibidos usando uma imagem desabilitada. Além disso, para botões de alternância, a imagem desabilitada é usada para indicar que o estado é desativado.

A imagem a seguir é um arquivo desabilitado típico.

![arquivo desabilitado](images/cesdkdis.png)

Isso armazena as imagens para botões de tipo de clique que estão desabilitados. As imagens são semelhantes ao arquivo de plano de fundo, mas as cores são mais claras. Usando o deslocamento definido na seção bitmaps do arquivo de definição de capa, as imagens de botão são alinhadas com a imagem do arquivo de plano de fundo.

Observe que o plano de fundo da imagem do botão corresponde exatamente à área correspondente no arquivo de plano de fundo. Isso é importante, porque quando um botão de tipo de ocorrência está indisponível, o retângulo inteiro definido para a imagem desabilitada substituirá a área correspondente no arquivo em segundo plano. Mantenha o gráfico consistente com a imagem de plano de fundo para garantir que apenas as partes do botão que você deseja que sejam diferentes sejam alteradas de fato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




