---
title: Arquivos de região
description: Arquivos de região
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Windows Media Player Capas móveis, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos de região
- Windows Media Player Capas móveis, arquivos de região
- capas, arquivos de região
- Arquivos de região em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ce26db27ef6ad3373916337c6378886a2846f71f1d8aa0e8d5266aae23eff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934063"
---
# <a name="region-files"></a>Arquivos de região

Os arquivos de região serão necessários se você usar qualquer tipo de botão de pressionamento (2PushHit, PushHit ou ToggleHit).

Os arquivos de região são usados para definir áreas que responderão a um toque, também conhecido como um pressionamento, em um botão específico. Para cada botão de clique, uma área no bitmap de região recebe uma cor da Web específica (como \# FF0000, que é o valor para vermelho sólido). O número de cor é especificado na definição do botão de região. Quando o usuário exibe a capa, a imagem do botão é sobreposta em segundo plano usando as coordenadas da área no bitmap da região.

Por exemplo, você pode desenhar um círculo vermelho em um local correspondente ao local do botão Next e colorir o vermelho sólido ( \# FF0000). Em seguida, na definição do botão, você pode atribuir um valor RGB de pressionamento de 255, 0, 0 (que é o equivalente RGB de \# FF0000). Nesse caso, o botão Avançar só responderia a toques (ocorrências) dentro do círculo vermelho.

Os botões de pressionamento são usados quando você deseja definir formas que não sejam retângulos. Você ainda deve definir as coordenadas para cada botão para que imagens secundárias, como push e Disabled, possam estar localizadas corretamente. Na prática, cada botão é limitado por um retângulo, e esses retângulos de limite imaginários não devem se sobrepor.

> [!Note]  
> os arquivos de arte de região não são necessários nas capas do Windows Media Player 10 mobile porque os tipos de botão não têm suporte no Windows Media Player 10 Mobile ou posterior.

 

A imagem a seguir é um arquivo de região típico.

![arquivo de região](images/cesdkreg.png)

Esse arquivo define as partes da capa para cada botão de tipo de clique. Cada cor será identificada por seu número de cor na seção botões do arquivo de definição de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivos de arte**](art-files-mobile.md)
</dt> </dl>

 

 




