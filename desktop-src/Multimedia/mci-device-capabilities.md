---
title: Recursos do dispositivo MCI
description: Recursos do dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Macro MCIWndCanConfig
- Macro MCIWndCanEject
- Macro MCIWndCanPlay
- Macro MCIWndCanRecord
- Macro MCIWndCanSave
- Macro MCIWndCanWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006069"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="5b2ca-109">Recursos do dispositivo MCI</span><span class="sxs-lookup"><span data-stu-id="5b2ca-109">MCI Device Capabilities</span></span>

<span data-ttu-id="5b2ca-110">O MCIWnd inclui as macros a seguir para permitir que você consulte os dispositivos MCI para obter seus recursos.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="5b2ca-111">Macro</span><span class="sxs-lookup"><span data-stu-id="5b2ca-111">Macro</span></span>                                      | <span data-ttu-id="5b2ca-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b2ca-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b2ca-113">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="5b2ca-114">Determina se um dispositivo tem uma caixa de diálogo de configuração para dar suporte a várias configurações, como o dispositivo MCIAVI.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="5b2ca-115">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="5b2ca-116">Determina se um dispositivo tem uma função de ejeção controlada por software.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="5b2ca-117">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="5b2ca-118">Determina se um dispositivo pode reproduzir o conteúdo existente.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="5b2ca-119">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="5b2ca-120">Determina se um dispositivo pode gravar.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="5b2ca-121">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="5b2ca-122">Determina se um dispositivo pode armazenar dados.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="5b2ca-123">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="5b2ca-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="5b2ca-124">Determina se um dispositivo dá suporte a comandos de janela MCI (como [**janela**](window.md), [**Put**](put.md) e [**Where**](where.md)).</span><span class="sxs-lookup"><span data-stu-id="5b2ca-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="5b2ca-125">Essas macros retornarão **true** se o dispositivo der suporte à capacidade específica ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5b2ca-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




