---
description: As funções a seguir são usadas com contextos de dispositivo.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Funções de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33eda03ce65a5873c4420f6675128243e30493dc75fa3055c8718f6826f4a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966046"
---
# <a name="device-context-functions"></a>Funções de contexto do dispositivo

As funções a seguir são usadas com contextos de dispositivo.



| Função                                                   | Descrição                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Cancela qualquer operação pendente no contexto do dispositivo especificado.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Altera as configurações do dispositivo de exibição padrão para o modo gráfico especificado.                                                        |
| [**Changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Altera as configurações do dispositivo de exibição especificado para o modo gráfico especificado.                                                      |
| [**Createcompatibledc**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Cria um contexto de dispositivo de memória compatível com o dispositivo especificado.                                                                     |
| [**Createdc**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Cria um contexto de dispositivo para um dispositivo usando o nome especificado.                                                                           |
| [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Cria um contexto de informações para o dispositivo especificado.                                                                                  |
| [**Deletedc**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Exclui o contexto do dispositivo especificado.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Exclui uma caneta lógica, pincel, fonte, bitmap, região ou paleta, liberando todos os recursos do sistema associados ao objeto.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Recupera os recursos de um driver de dispositivo de impressora.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Fornece recursos de desenho da exibição de vídeo especificada que não estão diretamente disponíveis por meio da interface do dispositivo gráfico.       |
| [**Enumdisplaydevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Recupera informações sobre os dispositivos de exibição em um sistema.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Recupera informações sobre um dos modos gráficos para um dispositivo de exibição.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Recupera informações sobre um dos modos gráficos para um dispositivo de exibição.                                                               |
| [**Enumobjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Enumera as canetas ou pincéis disponíveis para o contexto do dispositivo especificado.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Uma função de retorno de chamada definida pelo aplicativo usada com a [**função EnumObjects.**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Recupera um identificador para um objeto do tipo especificado que foi selecionado no contexto do dispositivo especificado.                           |
| [**Getdc**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Recupera um alça para um contexto de dispositivo de exibição para a área do cliente de uma janela especificada ou para toda a tela.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Recupera a cor do pincel atual para o contexto do dispositivo especificado.                                                                       |
| [**Getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Recupera um alça para um contexto de dispositivo de exibição para a área do cliente de uma janela especificada ou para toda a tela.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Recupera a origem da tradução final para um contexto de dispositivo especificado.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Recupera a cor da caneta atual para o contexto do dispositivo especificado.                                                                         |
| [**Getdevicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Recupera informações específicas do dispositivo para o dispositivo especificado.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Recupera o layout de um contexto de dispositivo.                                                                                                 |
| [**Getobject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Recupera informações para o objeto gráfico especificado.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Recupera o tipo do objeto especificado.                                                                                               |
| [**Getstockobject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Recupera um alça para uma das canetas de estoque, pincéis, fontes ou paletas.                                                                 |
| [**Releasedc**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Libera um contexto de dispositivo, liberando-o para uso por outros aplicativos.                                                                      |
| [**Resetdc**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Atualiza o contexto de dispositivo de plotagem ou impressora especificado usando as informações especificadas.                                                  |
| [**Restoredc**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Restaura um contexto de dispositivo para o estado especificado.                                                                                         |
| [**Savedc**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Salva o estado atual do contexto do dispositivo especificado copiando dados que descrevem objetos selecionados e modos gráficos para uma pilha de contexto. |
| [**Selectobject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Seleciona um objeto no contexto do dispositivo especificado.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Define a cor atual do pincel de contexto do dispositivo para o valor de cor especificado.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Define a cor da caneta de contexto do dispositivo atual para o valor de cor especificado.                                                                   |
| [**Setlayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Define o layout para um contexto de dispositivo.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Retorna um alça para a janela associada a um contexto de dispositivo.                                                                          |



 

 

 
