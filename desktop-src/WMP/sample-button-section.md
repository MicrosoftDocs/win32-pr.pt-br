---
title: Seção de botão de exemplo
description: Seção de botão de exemplo
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Aparências móveis do Windows Media Player, seção de botão
- capas, seção de botão
- referência para capas, seção de botão
- botões em capas, seção de botão
- arquivos de definição de capa, seção de botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005761"
---
# <a name="sample-button-section"></a>Seção de botão de exemplo

As linhas a seguir mostram uma seção de botões típicos de um arquivo de definição de capa:


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



Esse código define oito botões que são usados para fornecer todas as seguintes funções em uma capa:

-   Reproduzir, pausar e parar itens de mídia.
-   Embaralhar, repetir e percorrer a lista de reprodução.
-   Ativar mudo do volume.

Todos os botões, exceto o botão sem som, são botões de região. O botão mudo obtém suas imagens enviadas por push e desabilitadas do super bitmap para sua conveniência.

> [!Note]  
> Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior. Em vez de um tipo de botão declarado em seu arquivo de capa, digite "NA" para cada tipo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Botões**](buttons.md)
</dt> </dl>

 

 




