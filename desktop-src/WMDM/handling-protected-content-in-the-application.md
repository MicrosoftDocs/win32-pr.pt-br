---
title: Manipulando conteúdo protegido no aplicativo
description: Manipulando conteúdo protegido no aplicativo
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Mídia Gerenciador de Dispositivos, certificados
- Gerenciador de Dispositivos, certificados
- guia de programação, certificados
- aplicativos da área de trabalho, certificados
- criando Windows mídia Gerenciador de Dispositivos aplicativos,certificados
- certificates
- Windows Mídia Gerenciador de Dispositivos, conteúdo protegido por DRM
- Gerenciador de Dispositivos, conteúdo protegido por DRM
- guia de programação, conteúdo protegido por DRM
- aplicativos de área de trabalho, conteúdo protegido por DRM
- criando Windows de Gerenciador de Dispositivos mídia, conteúdo protegido por DRM
- Conteúdo protegido por DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0befd0eb9fe2fecf06235b0b9424776ed25f3b1c411439cac5ecdfa71910d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957366"
---
# <a name="handling-protected-content-in-the-application"></a>Manipulando conteúdo protegido no aplicativo

\[O Windows drm de mídia de mídia foi preterido e não deve ser usado. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) em vez disso.\]

Um aplicativo deve ter um certificado de transferência para ser capaz de lidar com o conteúdo protegido por DRM. Para saber onde obter esse certificado, consulte [Ferramentas para Desenvolvimento.](tools-for-development.md) Para lidar com conteúdo desprotegido, você pode usar um certificado fictício, conforme descrito [em Autenticando o aplicativo.](authenticating-the-application.md)

Antes de usar um dispositivo, seu aplicativo deve determinar se o dispositivo dá suporte Windows DRM de Mídia 10 para Dispositivos Portáteis e, em caso afirmatório, se os componentes drm são atuais. (Atual significa que o relógio seguro está correto e que o dispositivo foi individualizado corretamente.) Se o dispositivo não dá suporte a esta versão do DRM ou se ele não puder ser atualizado, você ainda poderá enviar arquivos para o dispositivo, mas eles podem não ser reproduzíveis, dependendo da versão da licença.

> [!Note]  
> No momento, não há suporte para a individualização de dispositivos.

 

Se seu aplicativo for link para Windows SDK de Formato de Mídia, ele precisará vincular à biblioteca Windows Formato de Mídia WMStubDRM.lib. Para obter mais informações sobre como chamar Windows de formato de mídia em conteúdo protegido por DRM, consulte "Habilitando o suporte a DRM" na documentação do SDK de Formato de Mídia do Windows. Observe que há um problema com a vinculação a Mssachlp.lib e WMStubDRM.lib. Isso é abordado no [artigo de KB 890079 no MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

O exemplo de código C++ a seguir determina se um dispositivo é um dispositivo Windows DRM de Mídia 10 e, em caso afirmatório, se o relógio está atualizado.

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



Se o dispositivo não for compatível com o Windows DRM de Mídia 10 para Dispositivos Portáteis e precisar ser atualizado (ou seja, se o valor de *status* no exemplo anterior não for simplesmente WMDM DEVICE ISWMDRM), o aplicativo deverá chamar \_ \_ [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passar o valor do *status* para executar as atualizações necessárias. O computador desktop deve estar conectado à Internet.

A função de exemplo C++ a seguir tenta atualizar um dispositivo DRM.


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

[**Criando um aplicativo Windows de Gerenciador de Dispositivos mídia**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Manipulando conteúdo protegido**](handling-protected-content.md)
</dt> </dl>

 

 