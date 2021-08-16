---
description: As funções a seguir são usadas para criar, alterar ou desenhar caminhos.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funções path (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700298056ac595b0e9208c0b8535d7a3d2e822e048e4c656d0b4501947764533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759422"
---
# <a name="path-functions-windows-gdi"></a>Funções path (Windows GDI)

As funções a seguir são usadas para criar, alterar ou desenhar caminhos.



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Fecha e descarta todos os caminhos no contexto do dispositivo especificado.                                                                                                   |
| [**Beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Abre um colchete de caminho no contexto do dispositivo especificado.                                                                                                            |
| [**Closefigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Fecha uma figura aberta em um caminho.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Fecha um colchete de caminho e seleciona o caminho definido pelo colchete no contexto do dispositivo especificado.                                                             |
| [**Fillpath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Fecha todas as figuras abertas no caminho atual e preenche o interior do caminho usando o pincel atual e o modo de preenchimento de polígono.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transforma todas as curvas no caminho selecionado no DC (contexto de dispositivo) atual, transformando cada curva em uma sequência de linhas.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera o limite de miter para o contexto do dispositivo especificado.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera as coordenadas que definem os pontos de extremidade de linhas e os pontos de controle de curvas encontrados no caminho selecionado no contexto do dispositivo especificado. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Cria uma região do caminho selecionado no contexto do dispositivo especificado.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Define o limite para o comprimento das junções de miter para o contexto do dispositivo especificado.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Fecha todas as figuras abertas em um caminho, traçou o contorno do caminho usando a caneta atual e preenche seu interior usando o pincel atual.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Renderiza o caminho especificado usando a caneta atual.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Redefine o caminho atual como a área que seria pintada se o caminho fosse traço usando a caneta selecionada atualmente no contexto do dispositivo determinado.            |



 

 

 



