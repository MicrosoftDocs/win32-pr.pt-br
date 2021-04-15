---
description: Cada exibição física é representada por um identificador de monitor do tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR e o contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988808"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="f3d72-103">HMONITOR e o contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f3d72-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="f3d72-104">Cada exibição física é representada por um identificador de monitor do tipo **HMONITOR**.</span><span class="sxs-lookup"><span data-stu-id="f3d72-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="f3d72-105">Uma **HMONITOR** válida é garantida como não nula.</span><span class="sxs-lookup"><span data-stu-id="f3d72-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="f3d72-106">Uma exibição física tem o mesmo **HMONITOR** , desde que faça parte da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3d72-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="f3d72-107">Quando uma mensagem do **WM \_ DISPLAYCHANGE** é enviada, qualquer monitor pode ser removido da área de trabalho e, portanto, seu **HMONITOR** se torna inválido ou tem suas configurações alteradas.</span><span class="sxs-lookup"><span data-stu-id="f3d72-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="f3d72-108">Portanto, um aplicativo deve verificar se todos os **HMONITORS** são válidos quando essa mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="f3d72-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="f3d72-109">Qualquer função que retorne um DC (contexto de dispositivo de exibição) normalmente retorna um DC para o monitor primário.</span><span class="sxs-lookup"><span data-stu-id="f3d72-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="f3d72-110">Para obter o controlador de domínio para outro monitor, use a função [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="f3d72-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="f3d72-111">Ou, você pode usar o nome do dispositivo da função [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para criar um controlador de domínio com [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="f3d72-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="f3d72-112">No entanto, se a função, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtém um DC para uma janela que abrange mais de uma exibição, o DC também abrangerá as duas exibições.</span><span class="sxs-lookup"><span data-stu-id="f3d72-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



