---
title: Habilitando PnP para dispositivos
description: Habilitando PnP para dispositivos
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Gerenciador de Dispositivos, dispositivos PnP
- Dispositivos Gerenciador de Dispositivos, PnP
- Guia de programação, dispositivos PnP
- provedores de serviço, dispositivos PnP
- criando provedores de serviços, dispositivos PnP
- Dispositivos PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822505"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="b8156-109">Habilitando PnP para dispositivos</span><span class="sxs-lookup"><span data-stu-id="b8156-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="b8156-110">O Windows Media Gerenciador de Dispositivos monitora as notificações de chegada e remoção de dispositivos que anunciam uma interface de dispositivo de player de áudio portátil.</span><span class="sxs-lookup"><span data-stu-id="b8156-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="b8156-111">Na chegada desse dispositivo, o Windows Media Gerenciador de Dispositivos consulta um parâmetro de dispositivo chamado *WMDMSPCLSID* para a ID de classe do provedor de serviços responsável por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8156-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="b8156-112">O Windows Media Gerenciador de Dispositivos chama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) neste provedor de serviços para criar um objeto de dispositivo, que é exposto ao aplicativo como um objeto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="b8156-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="b8156-113">Um provedor de serviços pode lidar com dispositivos PnP ou dispositivos não-PnP; Ele não pode lidar com ambos os tipos.</span><span class="sxs-lookup"><span data-stu-id="b8156-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="b8156-114">Para que um dispositivo funcione com o mecanismo anterior (e, portanto, habilite as notificações de chegada e remoção para o dispositivo em aplicativos Windows Media Gerenciador de Dispositivos), os seguintes requisitos devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="b8156-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="b8156-115">O driver de dispositivo deste dispositivo deve anunciar a interface de dispositivo do player de áudio portátil do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b8156-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="b8156-116">O GUID dessa interface de dispositivo é definido como:</span><span class="sxs-lookup"><span data-stu-id="b8156-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="b8156-117">Um dispositivo não deve anunciar essa interface se o dispositivo anunciar a interface de volume (definida como VolumeClassGuid ou \_ volume DEVINTERFACE GUID \_ em winioctl. h).</span><span class="sxs-lookup"><span data-stu-id="b8156-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="b8156-118">Se o dispositivo anunciar a interface de volume, ele já estará habilitado para PnP no Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b8156-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="b8156-119">-E/OU-</span><span class="sxs-lookup"><span data-stu-id="b8156-119">-AND/OR-</span></span>

    <span data-ttu-id="b8156-120">Uma nova subchave do registro para o provedor de serviços deve ser criada dentro da subchave HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media Gerenciador de dispositivos \\ KnownDevices.</span><span class="sxs-lookup"><span data-stu-id="b8156-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="b8156-121">Essa chave deve ter o nome do seu provedor de serviços e deve ter as duas entradas de valor do reg sz a seguir \_ :</span><span class="sxs-lookup"><span data-stu-id="b8156-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="b8156-122">O dispositivo deve ter um parâmetro de dispositivo chamado WMDMSPCLSID.</span><span class="sxs-lookup"><span data-stu-id="b8156-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="b8156-123">O valor desse parâmetro deve ser definido como o CLSID do provedor de serviços em um formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b8156-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="b8156-124">Para obter mais informações sobre os parâmetros do dispositivo, consulte [parâmetros do dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b8156-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="b8156-125">O valor do parâmetro deve ser o CLSID, não o ProgID do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b8156-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="b8156-126">O provedor de serviços para este dispositivo deve implementar a interface IMDServiceProvider2.</span><span class="sxs-lookup"><span data-stu-id="b8156-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="b8156-127">A chave do provedor de serviços em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media Gerenciador de dispositivos \\ plugins \\ SP \\ nome do serviço deve conter o seguinte valor DWORD</span><span class="sxs-lookup"><span data-stu-id="b8156-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b8156-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8156-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8156-129">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="b8156-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




