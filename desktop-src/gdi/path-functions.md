---
description: As funções a seguir são usadas para criar, alterar ou desenhar caminhos.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Funções de caminho (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967624"
---
# <a name="path-functions-windows-gdi"></a>Funções de caminho (GDI do Windows)

As funções a seguir são usadas para criar, alterar ou desenhar caminhos.



| Função                                       | Descrição                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Fecha e descarta todos os caminhos no contexto do dispositivo especificado.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Abre um colchete de caminho no contexto do dispositivo especificado.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Fecha uma figura aberta em um caminho.                                                                                                                                 |
| [**Caminho de fim**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Fecha um colchete de caminho e seleciona o caminho definido pelo colchete no contexto do dispositivo especificado.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Fecha as figuras abertas no caminho atual e preenche o interior do caminho usando o pincel atual e o modo de preenchimento de polígono.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transforma todas as curvas no caminho selecionado no contexto de dispositivo atual (DC), transformando cada curva em uma sequência de linhas.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Recupera o limite de mitra para o contexto de dispositivo especificado.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Recupera as coordenadas definindo os pontos de extremidade das linhas e os pontos de controle das curvas encontradas no caminho selecionado no contexto do dispositivo especificado. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Cria uma região a partir do caminho selecionado no contexto do dispositivo especificado.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Define o limite para o comprimento de junções de Mitre para o contexto de dispositivo especificado.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Fecha as figuras abertas em um caminho, traça o contorno do caminho usando a caneta atual e preenche seu interior usando o pincel atual.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Renderiza o caminho especificado usando a caneta atual.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Redefine o caminho atual como a área que será pintada se o caminho tivesse sido traçado usando a caneta selecionada no momento no contexto do dispositivo fornecido.            |



 

 

 



