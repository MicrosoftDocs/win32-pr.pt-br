---
description: Com alguns ajustes secundários em seu código, você pode enviar a saída do Windows GDI+ para uma impressora em vez de uma tela.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Impressão (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967751"
---
# <a name="printing-gdi"></a>Impressão (GDI+)

Com alguns ajustes secundários em seu código, você pode enviar a saída do Windows GDI+ para uma impressora em vez de uma tela. Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e passe esse identificador para um construtor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Coloque seus comandos de desenho em GDI+ entre chamadas para [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

Os tópicos a seguir abordam o envio de saída de GDI+ para impressoras com mais detalhes:

-   [Envio da saída GDI+ para uma impressora](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Exibindo uma caixa de diálogo de impressão](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Otimizar a impressão fornecendo um identificador de impressora](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



