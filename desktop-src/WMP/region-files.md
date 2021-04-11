---
title: Arquivos de região
description: Arquivos de região
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos de região
- Capas móveis do Windows Media Player, arquivos de região
- capas, arquivos de região
- Arquivos de região em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292717"
---
# <a name="region-files"></a>Arquivos de região

Os arquivos de região serão necessários se você usar qualquer tipo de botão de pressionamento (2PushHit, PushHit ou ToggleHit).

Os arquivos de região são usados para definir áreas que responderão a um toque, também conhecido como um pressionamento, em um botão específico. Para cada botão de clique, uma área no bitmap de região recebe uma cor da Web específica (como \# FF0000, que é o valor para vermelho sólido). O número de cor é especificado na definição do botão de região. Quando o usuário exibe a capa, a imagem do botão é sobreposta em segundo plano usando as coordenadas da área no bitmap da região.

Por exemplo, você pode desenhar um círculo vermelho em um local correspondente ao local do botão Next e colorir o vermelho sólido ( \# FF0000). Em seguida, na definição do botão, você pode atribuir um valor RGB de pressionamento de 255, 0, 0 (que é o equivalente RGB de \# FF0000). Nesse caso, o botão Avançar só responderia a toques (ocorrências) dentro do círculo vermelho.

Os botões de pressionamento são usados quando você deseja definir formas que não sejam retângulos. Você ainda deve definir as coordenadas para cada botão para que imagens secundárias, como push e Disabled, possam estar localizadas corretamente. Na prática, cada botão é limitado por um retângulo, e esses retângulos de limite imaginários não devem se sobrepor.

> [!Note]  
> Os arquivos de arte de região não são necessários nas capas móveis do Windows Media Player 10 porque os tipos de botão não têm suporte no Windows Media Player 10 Mobile ou posterior.

 

A imagem a seguir é um arquivo de região típico.

![arquivo de região](images/cesdkreg.png)

Esse arquivo define as partes da capa para cada botão de tipo de clique. Cada cor será identificada por seu número de cor na seção botões do arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




