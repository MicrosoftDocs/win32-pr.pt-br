---
title: Código completo para aparência simples
description: Código completo para aparência simples
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Criando capas, exemplos de código
- Capas do Windows Media Player, exemplos de código
- capas, exemplos de código
- arquivos de definição de capa, exemplos de código
- Criando capas, exemplos
- Capas do Windows Media Player, exemplos
- capas, exemplos
- arquivos de definição de capa, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822781"
---
# <a name="complete-code-for-simple-skin"></a>Código completo para aparência simples

Este é o código completo da primeira capa de exemplo:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



Agora você tem todas as peças reunidas.

Crie um arquivo compactado com uma extensão de nome de arquivo. zip. Esse arquivo compactado contém o arquivo de definição de capa, bitmaps e todos os arquivos de mídia digital que você deseja incluir. Renomeie o arquivo para que ele tenha uma extensão de nome de arquivo. wmz. Em seguida, clicar duas vezes em sua capa compactada a iniciará.

Você pode ver uma aparência semelhante de trabalho simples na seção de exemplos do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




