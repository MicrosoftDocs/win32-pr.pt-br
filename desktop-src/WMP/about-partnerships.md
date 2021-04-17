---
title: Sobre parcerias
description: Sobre parcerias
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, parcerias
- Modelo de objeto do Windows Media Player, parcerias
- modelo de objeto, parcerias
- Controle ActiveX do Windows Media Player, parcerias
- Controle ActiveX, parcerias
- Controle ActiveX móvel do Windows Media Player, parcerias
- Windows Media Player Mobile, parcerias
- Sincronizando dispositivos, parcerias
- sincronização de dispositivo, parcerias
- parcerias entre dispositivos e o Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104453846"
---
# <a name="about-partnerships"></a><span data-ttu-id="29635-113">Sobre parcerias</span><span class="sxs-lookup"><span data-stu-id="29635-113">About Partnerships</span></span>

<span data-ttu-id="29635-114">Uma parceria é uma relação especial entre um dispositivo portátil e o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="29635-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="29635-115">Os usuários podem estabelecer uma parceria para um dispositivo específico usando a interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="29635-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="29635-116">Você pode gerenciar parcerias programaticamente usando [IWMPSyncDevice:: Createpartnere](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span><span class="sxs-lookup"><span data-stu-id="29635-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="29635-117">O método **Createpartnership** inicia um processo assíncrono que termina quando o evento **CreatePartnershipComplete** é recebido por meio da interface **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="29635-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="29635-118">O Windows Media Player 10 ou posterior dá suporte à criação de parcerias com até 16 dispositivos.</span><span class="sxs-lookup"><span data-stu-id="29635-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="29635-119">Cada parceria tem um índice de parceria associado.</span><span class="sxs-lookup"><span data-stu-id="29635-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="29635-120">Você pode recuperar o índice de parceria para um dispositivo específico chamando [IWMPSyncDevice:: get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span><span class="sxs-lookup"><span data-stu-id="29635-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="29635-121">Os índices de parceria são numerados de 1 a 16.</span><span class="sxs-lookup"><span data-stu-id="29635-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="29635-122">Quando um dispositivo específico não tem uma parceria com o Windows Media Player, **getPartnershipIndex** retorna zero para o índice.</span><span class="sxs-lookup"><span data-stu-id="29635-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="29635-123">Você pode recuperar o status de parceria de um determinado dispositivo chamando [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e, em seguida, inspecionando o valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado.</span><span class="sxs-lookup"><span data-stu-id="29635-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="29635-124">O Windows Media Player permite que uma parceria com a biblioteca de um usuário em um computador para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29635-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="29635-125">Isso significa que a criação de uma nova parceria destrói qualquer parceria existente que o dispositivo atual pode ter com outro computador.</span><span class="sxs-lookup"><span data-stu-id="29635-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="29635-126">Para saber quando o status é alterado para um dispositivo, você pode receber o evento **DeviceStatusChange** .</span><span class="sxs-lookup"><span data-stu-id="29635-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="29635-127">O Windows Media Player não pode criar uma parceria com um dispositivo com o status **wmpdsManualDevice**.</span><span class="sxs-lookup"><span data-stu-id="29635-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29635-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29635-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29635-129">**Sobre a sincronização do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="29635-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="29635-130">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="29635-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="29635-131">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="29635-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




