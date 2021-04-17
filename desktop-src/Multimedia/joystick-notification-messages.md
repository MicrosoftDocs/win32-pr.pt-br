---
title: Mensagens de notificação de joystick
description: Mensagens de notificação de joystick
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- joysticks, notificações
- joysticks, mensagens
- joysticks, posição
- joysticks, botões
- MM_JOY1 mensagens
- MM_JOY2 mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770163"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="7c20d-109">Mensagens de notificação de joystick</span><span class="sxs-lookup"><span data-stu-id="7c20d-109">Joystick Notification Messages</span></span>

<span data-ttu-id="7c20d-110">As mensagens do joystick notificam seu aplicativo de que um joystick alterou a posição ou que um de seus botões alterou os Estados.</span><span class="sxs-lookup"><span data-stu-id="7c20d-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="7c20d-111">As mensagens que começam com MM \_ JOY1 serão enviadas para a função se seu aplicativo solicitar entrada do joystick usando o identificador JOYSTICKID1 e \_ as mensagens mm JOY2 forem enviadas se seu aplicativo solicitar entrada do joystick usando o identificador JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="7c20d-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="7c20d-112">As mensagens na tabela a seguir identificam o status dos botões do joystick:</span><span class="sxs-lookup"><span data-stu-id="7c20d-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="7c20d-113">Mensagem</span><span class="sxs-lookup"><span data-stu-id="7c20d-113">Message</span></span>                                         | <span data-ttu-id="7c20d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c20d-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="7c20d-115">**\_JOY1BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="7c20d-116">Um botão no joystick JOYSTICKID1 foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="7c20d-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="7c20d-117">**\_JOY1BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="7c20d-118">Foi lançado um botão no joystick JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="7c20d-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="7c20d-119">**\_JOY1MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="7c20d-120">O joystick JOYSTICKID1 alterou a posição na direção x ou y.</span><span class="sxs-lookup"><span data-stu-id="7c20d-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="7c20d-121">**\_JOY1ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="7c20d-122">O joystick JOYSTICKID1 alterou a posição na direção z.</span><span class="sxs-lookup"><span data-stu-id="7c20d-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="7c20d-123">**\_JOY2BUTTONDOWN mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="7c20d-124">Um botão no joystick JOYSTICKID2 foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="7c20d-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="7c20d-125">**\_JOY2BUTTONUP mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="7c20d-126">Foi lançado um botão no joystick JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="7c20d-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="7c20d-127">**\_JOY2MOVE mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="7c20d-128">O joystick JOYSTICKID2 alterou a posição na direção x ou y</span><span class="sxs-lookup"><span data-stu-id="7c20d-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="7c20d-129">**\_JOY2ZMOVE mm**</span><span class="sxs-lookup"><span data-stu-id="7c20d-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="7c20d-130">O joystick JOYSTICKID2 alterou a posição na direção z.</span><span class="sxs-lookup"><span data-stu-id="7c20d-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="7c20d-131">Todas as mensagens relatam botões inexistentes como liberadas.</span><span class="sxs-lookup"><span data-stu-id="7c20d-131">All messages report nonexistent buttons as released.</span></span>

 

 




