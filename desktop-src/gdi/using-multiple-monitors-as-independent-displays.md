---
description: Ao usar vários monitores como exibições independentes, a área de trabalho contém uma exibição ou um conjunto de exibições.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Usando monitores múltiplos como exibições independentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710672e02e8ea7244e09c21b876197033e5f17144433b8f530ad8e52cd6806e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468246"
---
# <a name="using-multiple-monitors-as-independent-displays"></a>Usando monitores múltiplos como exibições independentes

Ao usar vários monitores como exibições independentes, a área de trabalho contém uma exibição ou um conjunto de exibições. Esse conjunto de exibições sempre inclui o monitor primário e se comporta conforme mencionado nas outras seções deste tópico. Um aplicativo pode usar qualquer outro monitor como uma exibição independente.

> [!Note]  
> o uso de outros monitores como exibições independentes não tem suporte em drivers implementados para o Windows WDDM (modelo de Driver de vídeo).

 

O Gerenciador de janelas não sabe nada sobre as exibições independentes. Eles são totalmente controlados pelo aplicativo e nenhuma função do Gerenciador de janelas está disponível para o aplicativo (todas as chamadas do Gerenciador de janelas vão automaticamente para a exibição primária). Cada exibição independente tem sua própria origem e coordenadas horizontais e verticais, e é acessada por meio das funções GDI, como [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ou as funções do DirectX, como **DirectDrawCreate**.

Para localizar as exibições independentes, chame [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e procure o sinalizador exibições que não têm o \_ dispositivo de vídeo \_ anexado \_ ao \_ Desktop na estrutura do [**\_ dispositivo de vídeo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .

Um aplicativo pode abrir uma exibição chamando


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



Nesta chamada, o parâmetro *lpszDisplayName* é um dos nomes de dispositivo retornados por [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e *lpDevMode* é uma descrição do modo gráfico para este dispositivo. O HDC resultante pode ser usado para executar qualquer operação de gráficos para o dispositivo.

 

 



