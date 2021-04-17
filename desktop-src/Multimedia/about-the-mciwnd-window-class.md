---
title: Sobre a classe da janela MCIWnd
description: Sobre a classe da janela MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Classe de janela MCIWnd, sobre
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364043"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="7c3a2-105">Sobre a classe da janela MCIWnd</span><span class="sxs-lookup"><span data-stu-id="7c3a2-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="7c3a2-106">A classe de janela MCIWnd é fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="7c3a2-107">Usando uma única função, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) seu aplicativo pode criar um controle que reproduza qualquer dispositivo que use a interface de controle de mídia (MCI).</span><span class="sxs-lookup"><span data-stu-id="7c3a2-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="7c3a2-108">Esses dispositivos incluem áudio de CD, formato de onda-áudio, MIDI e dispositivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="7c3a2-109">Automatizar a reprodução também é rápido e fácil.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="7c3a2-110">Usando apenas uma função e duas macros, um aplicativo pode criar uma janela MCIWnd com o dispositivo de mídia apropriado, reproduzir o dispositivo e fechar o dispositivo e a janela quando o conteúdo tiver terminado a execução.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="7c3a2-111">Alguns dispositivos executam conteúdo armazenado em arquivos.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="7c3a2-112">Outros dispositivos, como dispositivos de CD de áudio, executam conteúdo que é armazenado em outra mídia.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="7c3a2-113">Para fins de clareza, essa visão geral se refere a ambas as circunstâncias como "reproduzir o dispositivo".</span><span class="sxs-lookup"><span data-stu-id="7c3a2-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




