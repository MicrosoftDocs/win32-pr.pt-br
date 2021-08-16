---
title: Código completo para a capa simples
description: Código completo para a capa simples
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- criando capas, exemplos de código
- Windows Media Player capas, exemplos de código
- capas, exemplos de código
- arquivos de definição de capa, exemplos de código
- criando capas, exemplos
- Windows Media Player capas,exemplos
- capas, exemplos
- arquivos de definição de capa, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b4d4380c6d7fb44290e8faff26bf5cb84dae552d09fe13594402dbe434ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135789"
---
# <a name="complete-code-for-simple-skin"></a>Código completo para a capa simples

Este é o código completo para a primeira capa de exemplo:


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



Agora você tem todas as partes juntas.

Crie um arquivo compactado com uma extensão .zip nome de arquivo. Esse arquivo compactado contém seu arquivo de definição de capa, bitmaps e todos os arquivos de mídia digital que você deseja incluir. Renomeie o arquivo para que ele tenha uma extensão de nome de arquivo .wmz. Em seguida, clicar duas vezes na capa compactada iniciará a reprodução.

Você pode ver uma capa simples de trabalho semelhante na seção de exemplos do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o arquivo de definição de capa**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




