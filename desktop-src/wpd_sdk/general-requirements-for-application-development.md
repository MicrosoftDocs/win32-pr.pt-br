---
description: Requisitos gerais para o desenvolvimento de aplicativos
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Requisitos gerais para o desenvolvimento de aplicativos (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170292"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="aebdd-103">Requisitos gerais para o desenvolvimento de aplicativos (API WPD)</span><span class="sxs-lookup"><span data-stu-id="aebdd-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="aebdd-104">Para criar um aplicativo de dispositivos portáteis do Windows, você deve ter o [SDK (Software Development Kit) do Windows](https://developer.microsoft.com/windows/downloads) instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="aebdd-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="aebdd-105">Os cabeçalhos e as bibliotecas necessárias aparecem na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="aebdd-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="aebdd-106">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="aebdd-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="aebdd-107">PortableDevice. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-107">PortableDevice.h</span></span>
-   <span data-ttu-id="aebdd-108">PortableDeviceTypes. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="aebdd-109">PortableDeviceApi. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="aebdd-110">Quaisquer outras bibliotecas necessárias e cabeçalhos exigidos pelo seu aplicativo para consumir ou processar arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="aebdd-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="aebdd-111">Se seu aplicativo der suporte às novas interfaces de serviços de dispositivo, ele também incluirá um ou mais dos seguintes arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="aebdd-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="aebdd-112">AnchorSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-113">BridgeDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-114">CalendarDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-115">ContactDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-116">Dispositivoservices. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-116">DeviceServices.h</span></span>
-   <span data-ttu-id="aebdd-117">FullEnumSyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-118">HintsDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-119">MessageDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-120">MetadataDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-121">NotesDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-122">RingtoneDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-123">StatusDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-124">SyncDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="aebdd-125">TaskDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="aebdd-125">TaskDeviceService.h</span></span>

<span data-ttu-id="aebdd-126">Dos arquivos na lista anterior, BridgeDeviceService. h e DeviceService. h são necessários para quase todos os aplicativos que dão suporte aos serviços de dispositivo; os outros arquivos definem tipos diferentes de serviços de dispositivo e seriam incluídos conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="aebdd-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aebdd-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aebdd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aebdd-128">**Dispositivos portáteis do Windows**</span><span class="sxs-lookup"><span data-stu-id="aebdd-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
