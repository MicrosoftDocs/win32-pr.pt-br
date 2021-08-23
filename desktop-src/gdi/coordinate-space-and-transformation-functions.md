---
description: As funções a seguir são usadas com espaços de coordenadas e transformações.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Funções de transformação e espaço de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe24e78002393d7a840e99d33840dfa4ba0d9e2ac89d941f998261955683e13f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718076"
---
# <a name="coordinate-space-and-transformation-functions"></a>Funções de transformação e espaço de coordenadas

As funções a seguir são usadas com espaços de coordenadas e transformações.



| Função                                                                       | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Clienttoscreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Converte as coordenadas da área do cliente de um ponto especificado em coordenadas de tela.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Concatena duas transformações de espaço do mundo para o espaço de página.                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Converte as coordenadas do dispositivo em coordenadas lógicas.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Recupera a posição atual em coordenadas lógicas.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Obtém as preferências de orientação da exibição.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Recupera o modo gráfico atual para o contexto do dispositivo especificado.                                                            |
| [**Getmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Recupera o modo de mapeamento atual.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Recupera a extensão x e a extensão y do viewport atual para o contexto do dispositivo especificado.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Recupera as coordenadas x e y da origem do viewport para o contexto do dispositivo especificado.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Recupera a extensão x e a extensão y da janela para o contexto do dispositivo especificado.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Recupera as coordenadas x e y da origem da janela para o contexto do dispositivo especificado.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Recupera o espaço do mundo atual para a transformação de espaço em página.                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Converte coordenadas lógicas em coordenadas de dispositivo.                                                                            |
| [**Mapwindowpoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Converte (mapeia) um conjunto de pontos de um espaço de coordenadas em relação a uma janela em um espaço de coordenadas em relação a outra janela. |
| [**Modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Altera a transformação de mundo para um contexto de dispositivo usando o modo especificado.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Modifica a origem do viewport para um contexto de dispositivo usando os deslocamentos horizontais e verticais especificados.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Modifica a origem da janela para um contexto de dispositivo usando os deslocamentos horizontais e verticais especificados.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Modifica o viewport para um contexto de dispositivo usando as taxas formadas pelos multiplicadores e divisores especificados.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Modifica a janela para um contexto de dispositivo usando as taxas formadas pelos multiplicadores e divisores especificados.                    |
| [**Screentoclient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Converte as coordenadas de tela de um ponto especificado na tela em coordenadas do cliente.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Define as preferências de orientação da exibição.                                                                                 |
| [**Setgraphicsmode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Define o modo gráfico para o contexto do dispositivo especificado.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Define o modo de mapeamento do contexto do dispositivo especificado.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Define as extensão horizontal e vertical do viewport para um contexto de dispositivo usando os valores especificados.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Especifica qual ponto do dispositivo é mapeado para a origem da janela (0,0).                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Define as extensão horizontal e vertical da janela para um contexto de dispositivo usando os valores especificados.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Especifica qual ponto de janela é mapeado para a origem do viewport (0,0).                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Define uma transformação linear bidimensional entre o espaço do mundo e o espaço de página para o contexto do dispositivo especificado.                |



 

 

 
