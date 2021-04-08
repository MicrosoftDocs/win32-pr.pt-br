---
description: As funções a seguir são usadas no gerenciamento de dispositivos.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Funções de gerenciamento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920315"
---
# <a name="device-management-functions"></a><span data-ttu-id="001e2-103">Funções de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="001e2-103">Device Management Functions</span></span>

<span data-ttu-id="001e2-104">As funções a seguir são usadas no gerenciamento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="001e2-104">The following functions are used in device management.</span></span>



| <span data-ttu-id="001e2-105">Função</span><span class="sxs-lookup"><span data-stu-id="001e2-105">Function</span></span>                                                             | <span data-ttu-id="001e2-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="001e2-106">Description</span></span>                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="001e2-107">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="001e2-107">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | <span data-ttu-id="001e2-108">Envia um código de controle diretamente para um driver de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="001e2-108">Sends a control code directly to a specified device driver.</span></span>                           |
| [<span data-ttu-id="001e2-109">**InstallNewDevice**</span><span class="sxs-lookup"><span data-stu-id="001e2-109">**InstallNewDevice**</span></span>](installnewdevice.md)                         | <span data-ttu-id="001e2-110">Instala um novo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="001e2-110">Installs a new device.</span></span> <span data-ttu-id="001e2-111">O usuário é solicitado a selecionar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="001e2-111">The user is prompted to select the device.</span></span>                     |
| [<span data-ttu-id="001e2-112">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="001e2-112">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | <span data-ttu-id="001e2-113">Registra o dispositivo ou tipo de dispositivo para o qual uma janela receberá notificações.</span><span class="sxs-lookup"><span data-stu-id="001e2-113">Registers the device or type of device for which a window will receive notifications.</span></span> |
| [<span data-ttu-id="001e2-114">**UnregisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="001e2-114">**UnregisterDeviceNotification**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | <span data-ttu-id="001e2-115">Fecha o identificador de notificação do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="001e2-115">Closes the specified device notification handle.</span></span>                                      |



 

<span data-ttu-id="001e2-116">As funções a seguir são usadas com unidades de CD-ROM e DVD.</span><span class="sxs-lookup"><span data-stu-id="001e2-116">The following functions are used with CD-ROM and DVD drives.</span></span>



| <span data-ttu-id="001e2-117">Função</span><span class="sxs-lookup"><span data-stu-id="001e2-117">Function</span></span>                                                               | <span data-ttu-id="001e2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="001e2-118">Description</span></span>                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="001e2-119">**CdromDisableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="001e2-119">**CdromDisableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | <span data-ttu-id="001e2-120">Desabilita a reprodução digital para a unidade de CD-ROM ou DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="001e2-120">Disables digital playback for the specified CD-ROM or DVD drive.</span></span>                                    |
| [<span data-ttu-id="001e2-121">**CdromEnableDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="001e2-121">**CdromEnableDigitalPlayback**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | <span data-ttu-id="001e2-122">Habilita a reprodução digital para a unidade de CD-ROM ou DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="001e2-122">Enables digital playback for the specified CD-ROM or DVD drive.</span></span>                                     |
| [<span data-ttu-id="001e2-123">**CdromIsDigitalPlaybackEnabled**</span><span class="sxs-lookup"><span data-stu-id="001e2-123">**CdromIsDigitalPlaybackEnabled**</span></span>](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | <span data-ttu-id="001e2-124">Determina se a reprodução digital está habilitada para a unidade de CD-ROM ou DVD especificada.</span><span class="sxs-lookup"><span data-stu-id="001e2-124">Determines whether digital playback is enabled for the specified CD-ROM or DVD drive.</span></span>               |
| [<span data-ttu-id="001e2-125">**CdromKnownGoodDigitalPlayback**</span><span class="sxs-lookup"><span data-stu-id="001e2-125">**CdromKnownGoodDigitalPlayback**</span></span>](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | <span data-ttu-id="001e2-126">Determina se a unidade de CD-ROM ou DVD especificada tem reprodução digital conhecida como boa.</span><span class="sxs-lookup"><span data-stu-id="001e2-126">Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.</span></span> |
| [<span data-ttu-id="001e2-127">**DvdLauncher**</span><span class="sxs-lookup"><span data-stu-id="001e2-127">**DvdLauncher**</span></span>](dvdlauncher.md)                                     | <span data-ttu-id="001e2-128">Verifica se a região de mídia na unidade de DVD corresponde à região da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="001e2-128">Verifies that the media region in the DVD drive matches the DVD drive region.</span></span>                       |



 

 

 
