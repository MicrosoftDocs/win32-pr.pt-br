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
# <a name="printing-gdi"></a><span data-ttu-id="41cd7-103">Impressão (GDI+)</span><span class="sxs-lookup"><span data-stu-id="41cd7-103">Printing (GDI+)</span></span>

<span data-ttu-id="41cd7-104">Com alguns ajustes secundários em seu código, você pode enviar a saída do Windows GDI+ para uma impressora em vez de uma tela.</span><span class="sxs-lookup"><span data-stu-id="41cd7-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="41cd7-105">Para desenhar em uma impressora, obtenha um identificador de contexto de dispositivo para a impressora e passe esse identificador para um construtor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="41cd7-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="41cd7-106">Coloque seus comandos de desenho em GDI+ entre chamadas para [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) e [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="41cd7-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="41cd7-107">Os tópicos a seguir abordam o envio de saída de GDI+ para impressoras com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="41cd7-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="41cd7-108">Envio da saída GDI+ para uma impressora</span><span class="sxs-lookup"><span data-stu-id="41cd7-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="41cd7-109">Exibindo uma caixa de diálogo de impressão</span><span class="sxs-lookup"><span data-stu-id="41cd7-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="41cd7-110">Otimizar a impressão fornecendo um identificador de impressora</span><span class="sxs-lookup"><span data-stu-id="41cd7-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



