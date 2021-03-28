---
description: As funções a seguir fornecem suporte para vários monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Várias funções de monitores de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967646"
---
# <a name="multiple-display-monitors-functions"></a>Várias funções de monitores de exibição

As funções a seguir fornecem suporte para vários monitores.



| Função                                           | Descrição                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera os monitores de exibição que interseccionam uma região formada pela interseção de um retângulo de recorte especificado e a região visível de um contexto de dispositivo. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera informações sobre um monitor de exibição.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Uma função de retorno de chamada definida pelo aplicativo que é chamada pela função [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera um identificador para o monitor de exibição que contém um ponto especificado.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera um identificador para o monitor de exibição que tem a maior área de interseção com um retângulo especificado.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera um identificador para o monitor de exibição que tem a maior área de interseção com o retângulo delimitador de uma janela especificada.                       |



 

 

 



