---
description: Cada monitor pode ter sua própria profundidade de cor.
ms.assetid: 8d1ba8d2-b43d-498d-be5a-100fe9fc0f61
title: Cores em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50410631cf0ea3ac0a1b9967f1116809be0a4851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921293"
---
# <a name="colors-on-multiple-display-monitors"></a><span data-ttu-id="02478-103">Cores em vários monitores de vídeo</span><span class="sxs-lookup"><span data-stu-id="02478-103">Colors on Multiple Display Monitors</span></span>

<span data-ttu-id="02478-104">Cada monitor pode ter sua própria profundidade de cor.</span><span class="sxs-lookup"><span data-stu-id="02478-104">Each monitor can have its own color depth.</span></span> <span data-ttu-id="02478-105">O sistema ajusta automaticamente as cores à medida que o Windows se move entre monitores com profundidades de cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="02478-105">The system automatically adjusts colors as windows move across monitors with different color depths.</span></span> <span data-ttu-id="02478-106">Em geral, isso produz bons resultados.</span><span class="sxs-lookup"><span data-stu-id="02478-106">In general, this produces good results.</span></span> <span data-ttu-id="02478-107">No entanto, isso nem sempre é o ideal.</span><span class="sxs-lookup"><span data-stu-id="02478-107">However, this is not always optimal.</span></span> <span data-ttu-id="02478-108">Para aproveitar os recursos de cores de monitores diferentes, consulte a seção [pintando vários monitores de vídeo](painting-on-multiple-display-monitors.md) , a seguir.</span><span class="sxs-lookup"><span data-stu-id="02478-108">To take advantage of the color capabilities of different monitors, see the [Painting on Multiple Display Monitors](painting-on-multiple-display-monitors.md) section that follows.</span></span>

<span data-ttu-id="02478-109">Para determinar se todos os monitores têm o mesmo formato de cor, chame [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ SAMEDISPLAYFORMAT.</span><span class="sxs-lookup"><span data-stu-id="02478-109">To determine if all monitors have the same color format, call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_SAMEDISPLAYFORMAT.</span></span>

<span data-ttu-id="02478-110">Se o monitor primário for palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) funcionam da mesma forma que antes, mas em todos os monitores.</span><span class="sxs-lookup"><span data-stu-id="02478-110">If the primary monitor is palettized, [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) and [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) work the same as before, but across all monitors.</span></span> <span data-ttu-id="02478-111">Além disso, as paletas de todos os dispositivos palettized são sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="02478-111">In addition, the palettes of all palettized devices are synchronized.</span></span> <span data-ttu-id="02478-112">Se o monitor primário não for palettized, **SelectPalette** e **RealizePalette** selecionarão a paleta em segundo plano e os dispositivos de palettized não serão sincronizados.</span><span class="sxs-lookup"><span data-stu-id="02478-112">If the primary monitor is not palettized, **SelectPalette** and **RealizePalette** will select the palette into the background and palettized devices will not be synchronized.</span></span>

 

 
