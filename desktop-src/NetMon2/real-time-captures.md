---
description: Os monitores recebem quadros de rede capturados no modo em tempo real. Os quadros são capturados por um NPP (provedor de pacotes de rede) usando a interface COM de provedores IRTC e passados para o monitor em um dos monitores dois threads de execução.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Capturas de Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837396"
---
# <a name="real-time-captures"></a><span data-ttu-id="27b38-104">Capturas de Real-Time</span><span class="sxs-lookup"><span data-stu-id="27b38-104">Real-Time Captures</span></span>

<span data-ttu-id="27b38-105">Os monitores recebem quadros de rede capturados no modo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="27b38-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="27b38-106">Os quadros são capturados por um NPP ( [*provedor de pacotes de rede*](n.md) ) usando a interface com do [IRTC](irtc.md) do provedor e passados para o monitor em um dos dois threads de execução do monitor.</span><span class="sxs-lookup"><span data-stu-id="27b38-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="27b38-107">Os monitores podem limitar o número de quadros que precisam ser processados, passando um [*filtro de captura*](c.md) para o NPP que está fornecendo os quadros.</span><span class="sxs-lookup"><span data-stu-id="27b38-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="27b38-108">Normalmente, um monitor específico é projetado para inspecionar tipos específicos de tráfego, como HTTP, RIPX ou SMB.</span><span class="sxs-lookup"><span data-stu-id="27b38-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="27b38-109">Ao contrário de especialistas, que usam analisadores sofisticados para selecionar as informações a serem analisadas, um monitor deve examinar cada quadro para as condições que ele foi projetado para detectar.</span><span class="sxs-lookup"><span data-stu-id="27b38-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="27b38-110">O motivo por trás dessa abordagem quadro a quadro é o desempenho.</span><span class="sxs-lookup"><span data-stu-id="27b38-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="27b38-111">Um monitor deve processar seus quadros rapidamente o bastante para que ele não fique atrás do driver fornecendo os quadros para o NPP.</span><span class="sxs-lookup"><span data-stu-id="27b38-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="27b38-112">Caso contrário, os dados serão perdidos.</span><span class="sxs-lookup"><span data-stu-id="27b38-112">Otherwise, data will be lost.</span></span>

 

 



