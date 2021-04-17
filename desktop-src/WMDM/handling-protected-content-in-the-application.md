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
# <a name="handling-protected-content-in-the-application"></a>Lidando com conteúdo protegido no aplicativo

\[O recurso DRM do Windows Media foi preterido e não deve ser usado. Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Um aplicativo deve ter um certificado de transferência para poder lidar com conteúdo protegido por DRM. Para saber onde obter esse certificado, consulte [ferramentas para desenvolvimento](tools-for-development.md). Para lidar com conteúdo desprotegido, você pode usar um certificado fictício conforme descrito em [Autenticando o aplicativo](authenticating-the-application.md).

Antes de usar um dispositivo, seu aplicativo deve determinar se o dispositivo dá suporte ao Windows Media DRM 10 para dispositivos portáteis e, nesse caso, que os componentes DRM são atuais. (Atual significa que o relógio seguro está correto e que o dispositivo foi individualmente individualizado.) Se o dispositivo não oferecer suporte a essa versão do DRM, ou se não puder ser atualizado, você ainda poderá enviar arquivos para o dispositivo, mas eles poderão não ser reproduzidos, dependendo da versão da licença.

> [!Note]  
> Atualmente, não há suporte para a individualização de dispositivos.

 

Se seu aplicativo for vinculado aos métodos do Windows Media Format SDK, ele precisará vincular-se à biblioteca de formatos de mídia do Windows WMStubDRM. lib. Para obter mais informações sobre como chamar métodos de formato de mídia do Windows em conteúdo protegido por DRM, consulte "Habilitando o suporte a DRM" na documentação do SDK do Windows Media Format. Observe que há um problema com a vinculação de Mssachlp. lib e WMStubDRM. lib. Isso é abordado no [artigo 890079 da base de conhecimento no MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

O exemplo de código C++ a seguir determina se um dispositivo é um dispositivo Windows Media DRM 10 e, em caso afirmativo, se o relógio está atualizado.

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



Se o dispositivo der suporte ao Windows Media DRM 10 para dispositivos portáteis e precisar ser atualizado (ou seja, se o valor do *status* no exemplo anterior não for simplesmente o WMDM \_ Device \_ ISWMDRM), o aplicativo deverá chamar [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor de *status* para executar as atualizações necessárias. O computador desktop deve estar conectado à Internet.

A seguinte função de exemplo C++ tenta atualizar um dispositivo DRM.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Lidando com conteúdo protegido**](handling-protected-content.md)
</dt> </dl>

 

 