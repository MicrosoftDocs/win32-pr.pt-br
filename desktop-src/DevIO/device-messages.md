---
description: Mensagens de dispositivo são mensagens do sistema que notificam aplicativos e outros recursos de eventos de alteração do dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Mensagens do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755410"
---
# <a name="device-messages"></a><span data-ttu-id="57ca4-103">Mensagens do dispositivo</span><span class="sxs-lookup"><span data-stu-id="57ca4-103">Device Messages</span></span>

<span data-ttu-id="57ca4-104">Mensagens de dispositivo são mensagens do sistema que notificam aplicativos e outros recursos de eventos de alteração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57ca4-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="57ca4-105">Esses eventos ocorrem sempre que o sistema detecta uma alteração no hardware do sistema, como quando o usuário encaixa e desencaixa um computador laptop, ou insere ou remove um dispositivo, como uma placa PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="57ca4-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="57ca4-106">Os eventos de dispositivo podem ocorrer enquanto o sistema está em execução ou quando o sistema retoma a operação depois de ser suspenso temporariamente.</span><span class="sxs-lookup"><span data-stu-id="57ca4-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="57ca4-107">Para ajudar a garantir que os aplicativos não percam dados quando os dispositivos ficarem indisponíveis, o sistema monitora a configuração de hardware e envia mensagens de dispositivo aos aplicativos para notificá-las das alterações e dar a ela a oportunidade de se preparar para as alterações antes que elas ocorram.</span><span class="sxs-lookup"><span data-stu-id="57ca4-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="57ca4-108">Para cada evento de dispositivo, o sistema transmite uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="57ca4-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="57ca4-109">Nessa mensagem, o parâmetro *wParam* identifica o [tipo de evento do dispositivo](device-event-types.md) e o parâmetro *lParam* é um ponteiro para dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="57ca4-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



