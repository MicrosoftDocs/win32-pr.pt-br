---
description: com alguns ajustes secundários em seu código, você pode enviar Windows GDI+ saída para uma impressora em vez de uma tela.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Imprimindo (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885077"
---
# <a name="printing-gdi"></a>Imprimindo (GDI+)

com alguns ajustes secundários em seu código, você pode enviar Windows GDI+ saída para uma impressora em vez de uma tela. Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e passe esse identificador para um construtor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . coloque seus GDI+ comandos de desenho entre chamadas para [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).

os tópicos a seguir abordam o envio GDI+ saída para impressoras com mais detalhes:

-   [Envio da saída GDI+ para uma impressora](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Exibindo uma caixa de diálogo de impressão](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Otimizar a impressão fornecendo um identificador de impressora](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



