---
description: Uma paleta de cores é uma matriz que contém valores de cor que identificam as cores que podem ser exibidas ou desenhadas no dispositivo de saída no momento.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Paletas de cores (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091202"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="e2fd0-103">Paletas de cores (GDI do Windows)</span><span class="sxs-lookup"><span data-stu-id="e2fd0-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="e2fd0-104">Uma paleta de cores é uma matriz que contém valores de cor que identificam as cores que podem ser exibidas ou desenhadas no dispositivo de saída no momento.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="e2fd0-105">As paletas de cores são usadas por dispositivos que são capazes de gerar muitas cores, mas que só podem exibir ou desenhar um subconjunto deles em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="e2fd0-106">Para esses dispositivos, o sistema mantém uma *paleta do sistema* para acompanhar e gerenciar as cores atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="e2fd0-107">Os aplicativos não têm acesso direto à paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="e2fd0-108">Em vez disso, o sistema associa uma paleta padrão a cada contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="e2fd0-109">Os aplicativos podem usar as cores na paleta padrão ou definir suas próprias cores criando *paletas lógicas* e associando-as a contextos de dispositivo individuais.</span><span class="sxs-lookup"><span data-stu-id="e2fd0-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="e2fd0-110">Um aplicativo pode determinar se um dispositivo dá suporte a paletas de cores verificando o \_ bit da paleta RC no valor RasterCaps retornado pela função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="e2fd0-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



