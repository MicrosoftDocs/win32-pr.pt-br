---
description: As funções a seguir oferecem suporte para vários monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funções de vários monitores de exibição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779136"
---
# <a name="multiple-display-monitors-functions"></a>Funções de vários monitores de exibição

As funções a seguir oferecem suporte para vários monitores.



| Função                                           | Descrição                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumdisplaymonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera monitores de exibição que cruzam uma região formada pela interseção de um retângulo de recorte especificado e a região visível de um contexto de dispositivo. |
| [**Getmonitorinfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera informações sobre um monitor de exibição.                                                                                                               |
| [**Monitorenumproc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Uma função de retorno de chamada definida pelo aplicativo que é chamada pela [**função EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera um alça para o monitor de exibição que contém um ponto especificado.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera um alça para o monitor de exibição que tem a maior área de interseção com um retângulo especificado.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera um alça para o monitor de exibição que tem a maior área de interseção com o retângulo delimitar de uma janela especificada.                       |



 

 

 



