---
title: Lidando com conteúdo protegido no aplicativo
description: Lidando com conteúdo protegido no aplicativo
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Gerenciador de Dispositivos de mídia do Windows, certificados
- Gerenciador de Dispositivos, certificados
- Guia de programação, certificados
- aplicativos de área de trabalho, certificados
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, certificados
- certificates
- Windows Media Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- Guia de programação, conteúdo protegido por DRM
- aplicativos de desktop, conteúdo protegido por DRM
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789593"
---
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="d9d97-115">Lidando com conteúdo protegido no aplicativo</span><span class="sxs-lookup"><span data-stu-id="d9d97-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="d9d97-116">\[O recurso DRM do Windows Media foi preterido e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="d9d97-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="d9d97-117">Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="d9d97-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="d9d97-118">Um aplicativo deve ter um certificado de transferência para poder lidar com conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="d9d97-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="d9d97-119">Para saber onde obter esse certificado, consulte [ferramentas para desenvolvimento](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="d9d97-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="d9d97-120">Para lidar com conteúdo desprotegido, você pode usar um certificado fictício conforme descrito em [Autenticando o aplicativo](authenticating-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="d9d97-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="d9d97-121">Antes de usar um dispositivo, seu aplicativo deve determinar se o dispositivo dá suporte ao Windows Media DRM 10 para dispositivos portáteis e, nesse caso, que os componentes DRM são atuais.</span><span class="sxs-lookup"><span data-stu-id="d9d97-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="d9d97-122">(Atual significa que o relógio seguro está correto e que o dispositivo foi individualmente individualizado.) Se o dispositivo não oferecer suporte a essa versão do DRM, ou se não puder ser atualizado, você ainda poderá enviar arquivos para o dispositivo, mas eles poderão não ser reproduzidos, dependendo da versão da licença.</span><span class="sxs-lookup"><span data-stu-id="d9d97-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="d9d97-123">Atualmente, não há suporte para a individualização de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d9d97-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="d9d97-124">Se seu aplicativo for vinculado aos métodos do Windows Media Format SDK, ele precisará vincular-se à biblioteca de formatos de mídia do Windows WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="d9d97-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="d9d97-125">Para obter mais informações sobre como chamar métodos de formato de mídia do Windows em conteúdo protegido por DRM, consulte "Habilitando o suporte a DRM" na documentação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d9d97-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="d9d97-126">Observe que há um problema com a vinculação de Mssachlp. lib e WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="d9d97-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="d9d97-127">Isso é abordado no [artigo 890079 da base de conhecimento no MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span><span class="sxs-lookup"><span data-stu-id="d9d97-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="d9d97-128">O exemplo de código C++ a seguir determina se um dispositivo é um dispositivo Windows Media DRM 10 e, em caso afirmativo, se o relógio está atualizado.</span><span class="sxs-lookup"><span data-stu-id="d9d97-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



<span data-ttu-id="d9d97-129">Se o dispositivo der suporte ao Windows Media DRM 10 para dispositivos portáteis e precisar ser atualizado (ou seja, se o valor do *status* no exemplo anterior não for simplesmente o WMDM \_ Device \_ ISWMDRM), o aplicativo deverá chamar [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor de *status* para executar as atualizações necessárias.</span><span class="sxs-lookup"><span data-stu-id="d9d97-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="d9d97-130">O computador desktop deve estar conectado à Internet.</span><span class="sxs-lookup"><span data-stu-id="d9d97-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="d9d97-131">A seguinte função de exemplo C++ tenta atualizar um dispositivo DRM.</span><span class="sxs-lookup"><span data-stu-id="d9d97-131">The following C++ example function attempts to update a DRM device.</span></span>


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d9d97-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9d97-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9d97-133">**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="d9d97-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="d9d97-134">**Lidando com conteúdo protegido**</span><span class="sxs-lookup"><span data-stu-id="d9d97-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 