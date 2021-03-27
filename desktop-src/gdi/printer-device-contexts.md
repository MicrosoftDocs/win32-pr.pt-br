---
description: O controlador de domínio da impressora pode ser usado ao imprimir em uma impressora matricial, impressora jato de tinta, impressora laser ou plotadora.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextos de dispositivo de impressora (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967609"
---
# <a name="printer-device-contexts-windows-gdi"></a><span data-ttu-id="6b269-103">Contextos de dispositivo de impressora (GDI do Windows)</span><span class="sxs-lookup"><span data-stu-id="6b269-103">Printer Device Contexts (Windows GDI)</span></span>

<span data-ttu-id="6b269-104">O controlador de domínio da impressora pode ser usado ao imprimir em uma impressora matricial, impressora jato de tinta, impressora laser ou plotadora.</span><span class="sxs-lookup"><span data-stu-id="6b269-104">The printer DC can be used when printing on a dot-matrix printer, ink-jet printer, laser printer, or plotter.</span></span> <span data-ttu-id="6b269-105">Um aplicativo cria um DC de impressora chamando a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) e fornecendo os argumentos apropriados (o nome do driver de impressora, o nome da impressora, o nome do arquivo ou do dispositivo para a mídia de saída física e outros dados de inicialização).</span><span class="sxs-lookup"><span data-stu-id="6b269-105">An application creates a printer DC by calling the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function and supplying the appropriate arguments (the name of the printer driver, the name of the printer, the file or device name for the physical output medium, and other initialization data).</span></span> <span data-ttu-id="6b269-106">Quando um aplicativo termina de imprimir, ele exclui o controlador de domínio da impressora chamando a função [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="6b269-106">When an application has finished printing, it deletes the printer DC by calling the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span> <span data-ttu-id="6b269-107">Um aplicativo deve excluir (em vez de liberar) um controlador de domínio de impressora; a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) falha quando um aplicativo tenta usá-lo para liberar um controlador de domínio de impressora.</span><span class="sxs-lookup"><span data-stu-id="6b269-107">An application must delete (rather than release) a printer DC; the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function fails when an application attempts to use it to release a printer DC.</span></span>

<span data-ttu-id="6b269-108">Para obter mais informações, consulte [saída da impressora](../printdocs/printer-output.md).</span><span class="sxs-lookup"><span data-stu-id="6b269-108">For more information, see [Printer Output](../printdocs/printer-output.md).</span></span>

 

 
