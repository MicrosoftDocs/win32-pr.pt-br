---
title: Dispositivos Touchpad do Windows Precision
description: Dispositivos Touchpad do Windows Precision
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104365426"
---
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="13378-103">Dispositivos Touchpad do Windows Precision</span><span class="sxs-lookup"><span data-stu-id="13378-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="13378-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="13378-104">Platforms</span></span>

<dl> <span data-ttu-id="13378-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13378-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="13378-106">Description</span><span class="sxs-lookup"><span data-stu-id="13378-106">Description</span></span>

<span data-ttu-id="13378-107">O touchpad do Windows Precision é uma nova classe de dispositivos de entrada que fornece funcionalidade de gesto e entrada de ponteiro de alta precisão.</span><span class="sxs-lookup"><span data-stu-id="13378-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="13378-108">Por padrão, esses dispositivos geram mensagens de roda de rolagem de precisão extremamente alta para o consumo de aplicativos de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="13378-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="13378-109">Manifestações</span><span class="sxs-lookup"><span data-stu-id="13378-109">Manifestations</span></span>

<span data-ttu-id="13378-110">Os aplicativos que não foram projetados para lidar com mensagens de roda de rolagem de precisão extremamente alta podem sobrerolar ou não rolar corretamente.</span><span class="sxs-lookup"><span data-stu-id="13378-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="13378-111">Atenuação</span><span class="sxs-lookup"><span data-stu-id="13378-111">Mitigation</span></span>

<span data-ttu-id="13378-112">Os desenvolvedores de aplicativos devem examinar o Delta de rolagem nas mensagens da roda de rolagem do mouse e modificar seus aplicativos adequadamente; no entanto, no interim, um aplicativo pode recusar mensagens de roda de rolagem de precisão extremamente alta (Delta = 1) e escolher para receber mensagens de roda de rolagem de alta precisão (Delta = 40) ou mensagens de roda de rolagem padrão (Delta = 120).</span><span class="sxs-lookup"><span data-stu-id="13378-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="13378-113">Solução</span><span class="sxs-lookup"><span data-stu-id="13378-113">Solution</span></span>

<span data-ttu-id="13378-114">Se o aplicativo for capaz de lidar com mensagens de roda de rolagem de precisão extremamente alta, nada precisará ser feito, pois essa é a mensagem padrão enviada pelos touchpads do Windows Precision.</span><span class="sxs-lookup"><span data-stu-id="13378-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="13378-115">Se o aplicativo for capaz de lidar com mensagens de roda de rolagem de alta precisão, mas não para mensagens de roda de precisão ultra alta, adicione o seguinte ao manifesto do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="13378-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="13378-116">Se o aplicativo não for capaz de lidar com mensagens de roda de rolagem de alta precisão ou mensagens de roda de precisão extremamente alta, adicione o seguinte ao manifesto do aplicativo para indicar que as mensagens de roda de rolagem padrão são desejadas:</span><span class="sxs-lookup"><span data-stu-id="13378-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




