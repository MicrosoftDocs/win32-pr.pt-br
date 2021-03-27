---
description: As funções a seguir são usadas com espaços de coordenadas e transformações.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Funções de transformação e espaço de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e561f5cc9784439f5bef4f696e98d5919cb052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165086"
---
# <a name="coordinate-space-and-transformation-functions"></a>Funções de transformação e espaço de coordenadas

As funções a seguir são usadas com espaços de coordenadas e transformações.



| Função                                                                       | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Converte as coordenadas da área do cliente de um ponto especificado em coordenadas da tela.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Concatena duas transformações de espaço no mundo para página-espaço.                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Converte coordenadas de dispositivo em coordenadas lógicas.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Recupera a posição atual em coordenadas lógicas.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Obtém as preferências de orientação da exibição.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Recupera o modo gráfico atual para o contexto do dispositivo especificado.                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Recupera o modo de mapeamento atual.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Recupera a extensão x e a extensão y do visor atual para o contexto do dispositivo especificado.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Recupera as coordenadas x e y da origem do visor para o contexto do dispositivo especificado.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Recupera a extensão x e a extensão y da janela para o contexto do dispositivo especificado.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Recupera as coordenadas x e y da origem da janela para o contexto do dispositivo especificado.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Recupera a transformação espaço mundial atual para a página-espaço.                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Converte coordenadas lógicas em coordenadas do dispositivo.                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Converte (mapeia) um conjunto de pontos de um espaço de coordenadas em relação a uma janela para um espaço de coordenadas em relação a outra janela. |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Altera a transformação mundial para um contexto de dispositivo usando o modo especificado.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Modifica a origem do visor para um contexto de dispositivo usando os deslocamentos horizontal e vertical especificados.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Modifica a origem da janela para um contexto de dispositivo usando os deslocamentos horizontal e vertical especificados.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Modifica o visor para um contexto de dispositivo usando as proporções formadas pelos multiplicands e divisores especificados.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Modifica a janela para um contexto de dispositivo usando as proporções formadas pelos multiplicands e divisores especificados.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Converte as coordenadas de tela de um ponto especificado na tela para as coordenadas do cliente.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Define as preferências de orientação da exibição.                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Define o modo gráfico para o contexto do dispositivo especificado.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Define o modo de mapeamento do contexto do dispositivo especificado.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Define as extensões horizontais e verticais do visor para um contexto de dispositivo usando os valores especificados.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Especifica qual ponto de dispositivo mapeia para a origem da janela (0, 0).                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Define as extensões horizontais e verticais da janela para um contexto de dispositivo usando os valores especificados.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Especifica qual ponto de janela é mapeado para a origem do visor (0, 0).                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Define uma transformação linear bidimensional entre o espaço mundial e o espaço da página para o contexto do dispositivo especificado.                |



 

 

 
