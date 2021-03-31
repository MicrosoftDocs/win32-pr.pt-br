---
title: Referência de joystick
description: Referência de joystick
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Multimídia do Windows, referência de joystick
- multimídia, referência de joystick
- entrada de multimídia, referência de joystick
- joysticks, referência
- referência para joysticks, sobre
- referência de joystick, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823692"
---
# <a name="joystick-reference"></a><span data-ttu-id="eb500-109">Referência de joystick</span><span class="sxs-lookup"><span data-stu-id="eb500-109">Joystick Reference</span></span>

<span data-ttu-id="eb500-110">Esta seção descreve as funções, as estruturas e as mensagens associadas a joysticks.</span><span class="sxs-lookup"><span data-stu-id="eb500-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="eb500-111">Os elementos são agrupados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="eb500-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="eb500-112">Funcionalidades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="eb500-112">Device Capabilities</span></span>

-   [<span data-ttu-id="eb500-113">**joyGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="eb500-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="eb500-114">**joyGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="eb500-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="eb500-115">**JOYCAPS**</span><span class="sxs-lookup"><span data-stu-id="eb500-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="eb500-116">Consultando um joystick</span><span class="sxs-lookup"><span data-stu-id="eb500-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="eb500-117">**joyConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="eb500-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="eb500-118">**joyGetPos**</span><span class="sxs-lookup"><span data-stu-id="eb500-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="eb500-119">**joyGetPosEx**</span><span class="sxs-lookup"><span data-stu-id="eb500-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="eb500-120">**JOYINFO**</span><span class="sxs-lookup"><span data-stu-id="eb500-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="eb500-121">**JOYINFOEX**</span><span class="sxs-lookup"><span data-stu-id="eb500-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="eb500-122">Capturando um joystick</span><span class="sxs-lookup"><span data-stu-id="eb500-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="eb500-123">**joyGetThreshold**</span><span class="sxs-lookup"><span data-stu-id="eb500-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="eb500-124">**joyReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="eb500-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="eb500-125">**joySetCapture**</span><span class="sxs-lookup"><span data-stu-id="eb500-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="eb500-126">**joySetThreshold**</span><span class="sxs-lookup"><span data-stu-id="eb500-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="eb500-127">**\_JOY1BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="eb500-128">**\_JOY1BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="eb500-129">**\_JOY1MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="eb500-130">**\_JOY1ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="eb500-131">**\_JOY2BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="eb500-132">**\_JOY2BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="eb500-133">**\_JOY2MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="eb500-134">**\_JOY2ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="eb500-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="eb500-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb500-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb500-136">Joysticks</span><span class="sxs-lookup"><span data-stu-id="eb500-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 