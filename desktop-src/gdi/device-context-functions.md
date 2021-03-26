---
description: As funções a seguir são usadas com contextos de dispositivo.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Funções de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625b81b999526d84af4b58f2dddbc280643bcd35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661621"
---
# <a name="device-context-functions"></a>Funções de contexto do dispositivo

As funções a seguir são usadas com contextos de dispositivo.



| Função                                                   | Descrição                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Cancela qualquer operação pendente no contexto de dispositivo especificado.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Altera as configurações do dispositivo de vídeo padrão para o modo gráfico especificado.                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Altera as configurações do dispositivo de vídeo especificado para o modo gráfico especificado.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Cria um contexto de dispositivo de memória compatível com o dispositivo especificado.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Cria um contexto de dispositivo para um dispositivo usando o nome especificado.                                                                           |
| [**Criar**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Cria um contexto de informações para o dispositivo especificado.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Exclui o contexto do dispositivo especificado.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Exclui uma caneta lógica, um pincel, uma fonte, um bitmap, uma região ou uma paleta, liberando todos os recursos do sistema associados ao objeto.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Recupera os recursos de um driver de dispositivo de impressora.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Fornece recursos de desenho da tela de vídeo especificada que não estão diretamente disponíveis por meio da interface de dispositivo de gráficos.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Recupera informações sobre os dispositivos de vídeo em um sistema.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Recupera informações sobre um dos modos gráficos para um dispositivo de vídeo.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Recupera informações sobre um dos modos gráficos para um dispositivo de vídeo.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Enumera as canetas ou os pincéis disponíveis para o contexto do dispositivo especificado.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Uma função de retorno de chamada definida pelo aplicativo usada com a função [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .                                       |
| [**Getactualobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Recupera um identificador para um objeto do tipo especificado que foi selecionado no contexto do dispositivo especificado.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Recupera um identificador para um contexto de dispositivo de exibição para a área do cliente de uma janela especificada ou para toda a tela.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Recupera a cor do pincel atual para o contexto do dispositivo especificado.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Recupera um identificador para um contexto de dispositivo de exibição para a área do cliente de uma janela especificada ou para toda a tela.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Recupera a origem da tradução final para um contexto de dispositivo especificado.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Recupera a cor da caneta atual para o contexto do dispositivo especificado.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Recupera informações específicas do dispositivo para o dispositivo especificado.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Recupera o layout de um contexto de dispositivo.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Recupera informações para o objeto gráfico especificado.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Recupera o tipo do objeto especificado.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Recupera um identificador para uma das canetas, pincéis, fontes ou paletas de ações.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Libera um contexto de dispositivo, liberando-o para uso por outros aplicativos.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Atualiza o contexto da impressora ou do dispositivo de plotadora especificado usando as informações especificadas.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Restaura um contexto de dispositivo para o estado especificado.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Salva o estado atual do contexto do dispositivo especificado copiando os dados que descrevem os objetos selecionados e os modos gráficos em uma pilha de contexto. |
| [**Selecionarobject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Seleciona um objeto no contexto do dispositivo especificado.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Define a cor do pincel de contexto do dispositivo atual como o valor de cor especificado.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Define a cor da caneta de contexto do dispositivo atual como o valor de cor especificado.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Define o layout de um contexto de dispositivo.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Retorna um identificador para a janela associada a um contexto de dispositivo.                                                                          |



 

 

 
