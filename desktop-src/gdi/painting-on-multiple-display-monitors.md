---
description: O sistema manipula automaticamente a pintura em um DC (contexto de dispositivo) que abrange mais de um monitor, mesmo quando os monitores têm profundidades de cores diferentes.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Pintando em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661592"
---
# <a name="painting-on-multiple-display-monitors"></a>Pintando em vários monitores de vídeo

O sistema manipula automaticamente a pintura em um DC (contexto de dispositivo) que abrange mais de um monitor, mesmo quando os monitores têm profundidades de cores diferentes. Geralmente, isso produz bons resultados, mas pode não ser o ideal. Por exemplo, uma janela em dois monitores de profundidades de cores muito diferentes poderia ter uma representação de cor ruim. Além disso, monitores com a mesma intensidade de cor podem ter um exemplo de formatsfor de cor diferente, as cores podem ser codificadas com diferentes números de bits ou estar localizadas em locais diferentes no valor de cor de um pixel.

Para obter os melhores resultados para cada um dos monitores em um DC que abrange mais de uma exibição, chame [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) para enumerar os monitores que interseccionam seu controlador de domínio e pinte a área de interseção em cada um deles separadamente de acordo com os atributos de exibição desse monitor. Consulte o exemplo em [pintura em um DC que abrange vários monitores](painting-on-a-dc-that-spans-multiple-displays.md).

Se você fizer todo o desenho em seu código **de \_ pintura do WM** e se o código de **\_ pintura do WM** tratar de todos os vários modos de vídeo, você deverá ser capaz de posicionar o código de **\_ pintura do WM** no **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) com apenas algumas modificações.

 

 



