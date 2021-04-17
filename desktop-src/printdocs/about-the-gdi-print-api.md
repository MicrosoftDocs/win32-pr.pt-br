---
description: Um dos principais recursos das funções na API de impressão GDI é o suporte da independência do dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Sobre a API de impressão GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797551"
---
# <a name="about-the-gdi-print-api"></a><span data-ttu-id="ae831-103">Sobre a API de impressão GDI</span><span class="sxs-lookup"><span data-stu-id="ae831-103">About the GDI Print API</span></span>

<span data-ttu-id="ae831-104">Um dos principais recursos das funções na API de impressão GDI é o suporte da independência do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae831-104">One of the chief features of the functions in the GDI print API is their support of device independence.</span></span> <span data-ttu-id="ae831-105">Em vez de emitir comandos específicos do dispositivo para desenhar a saída em uma determinada impressora ou plotadora, um aplicativo chama funções de alto nível da interface gráfica do dispositivo (GDI).</span><span class="sxs-lookup"><span data-stu-id="ae831-105">Instead of issuing device-specific commands to draw output on a particular printer or plotter, an application calls high-level functions from the graphics device interface (GDI).</span></span> <span data-ttu-id="ae831-106">Por exemplo, para imprimir uma imagem de bitmap, um aplicativo pode chamar a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , fornecendo as coordenadas para o bitmap, bem como identificadores que identificam os DCS (contextos de dispositivo de origem e de destino).</span><span class="sxs-lookup"><span data-stu-id="ae831-106">For example, to print a bitmapped image, an application can call the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function, supplying the coordinates for the bitmap as well as handles identifying the source and destination device contexts (DCs).</span></span> <span data-ttu-id="ae831-107">A chamada para **BitBlt** é então convertida em comandos de dispositivo bruto por um driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="ae831-107">The call to **BitBlt** is then converted to raw device commands by a printer driver.</span></span> <span data-ttu-id="ae831-108">Um driver de dispositivo é uma DLL (biblioteca de vínculo dinâmico) que dá suporte à DDI (interface de driver de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="ae831-108">A device driver is a dynamic-link library (DLL) that supports the device driver interface (DDI).</span></span> <span data-ttu-id="ae831-109">Um driver de dispositivo gera comandos de dispositivo brutos quando processa chamadas para funções de DDI feitas pelo mecanismo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ae831-109">A device driver generates raw device commands when it processes calls to DDI functions made by the graphics engine.</span></span> <span data-ttu-id="ae831-110">Os comandos são processados pela impressora quando ele imprime a imagem.</span><span class="sxs-lookup"><span data-stu-id="ae831-110">The commands are processed by the printer when it prints the image.</span></span> <span data-ttu-id="ae831-111">A sintaxe, o número e o tipo desses comandos variam de dispositivo para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae831-111">The syntax, number, and type of these commands vary from device to device.</span></span>

<span data-ttu-id="ae831-112">Esta visão geral fornece informações sobre os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae831-112">This overview provides information on the following topics.</span></span>

<dl>

[<span data-ttu-id="ae831-113">Interface de impressão padrão</span><span class="sxs-lookup"><span data-stu-id="ae831-113">Default Printing Interface</span></span>](default-printing-interface.md)  
[<span data-ttu-id="ae831-114">Contextos de dispositivo de impressora</span><span class="sxs-lookup"><span data-stu-id="ae831-114">Printer Device Contexts</span></span>](printer-output.md)  
[<span data-ttu-id="ae831-115">Escapes de impressora</span><span class="sxs-lookup"><span data-stu-id="ae831-115">Printer Escapes</span></span>](printer-escapes.md)  
[<span data-ttu-id="ae831-116">Exibição e saída WYSIWYG</span><span class="sxs-lookup"><span data-stu-id="ae831-116">WYSIWYG Display and Output</span></span>](wysiwyg-display-and-output.md)  
[<span data-ttu-id="ae831-117">DEVMODE por usuário</span><span class="sxs-lookup"><span data-stu-id="ae831-117">Per-User DEVMODE</span></span>](per-user-devmode.md)  
</dl>

 

 
