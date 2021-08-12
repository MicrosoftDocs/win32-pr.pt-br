---
description: Testando se um driver de gráfico dá suporte ao COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Testando se um driver de gráfico dá suporte ao COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22280f880ba01a8e51acda74a2a46dff595d5569f885ce1da3a3631bacd8db06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651826"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a>Testando se um driver de gráfico dá suporte ao COPP

O COPP (Certified Output Protection Protocol) permite que um aplicativo proteja o conteúdo do vídeo à medida que ele vai da placa de vídeo para o dispositivo de exibição. Se um driver de gráficos dá suporte ao COPP, o driver mantém uma cadeia de certificados, assinada pela Microsoft, autenticando o driver. Os aplicativos de reprodução que usam o COPP para impor a proteção de conteúdo devem validar a cadeia de certificados para garantir que o driver não tenha sido adulterado.

No entanto, talvez você queira verificar se um driver de gráficos dá suporte ao COPP, sem validar o certificado. Por exemplo, quando um provedor de mídia digital emite uma licença drm (gerenciamento de direitos digitais), talvez ele queira verificar se o usuário tem um driver gráfico habilitado para COPP. O provedor não precisa impor o COPP no momento em que emite a licença; ele só precisa testar se o driver dá suporte ao COPP.

O código a seguir mostra como testar se um driver dá suporte ao COPP. O aplicativo deve passar o nome de um arquivo de vídeo que será usado para testar o driver. Isso é necessário porque o filtro renderizado de combinação de vídeo na Microsoft® DirectShow® inicializa uma sessão COPP até que o filtro esteja conectado. Essa função pode ser incluída em um aplicativo cliente para verificar se o driver é capaz de executar o COPP.

> [!Note]  
> Se o computador do usuário tiver duas placas gráficas, essa função testa o driver para a placa gráfica primária, mas não a placa gráfica secundária.

 


```C++
#include <dshow.h>
// Link to strmiids.lib

#define SAFE_RELEASE(p) if (NULL != (p)) { (p)->Release(); (p) = NULL; }
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }

enum COPPSupport 
{
    SUPPORTS_COPP,
    DOES_NOT_SUPPORT_COPP,
    CANNOT_DETERMINE_COPP_SUPPORT
};

//------------------------------------------------------------------------
// Name:        IsDriverCoppEnabled
// Description: Test whether the user's graphics driver supports
//              COPP.
// wszTestFile: Name of a video file to use for testing.
//
// If this method returns the value SUPPORTS_COPP, it does *not* guarantee 
// that the driver is a valid COPP-enabled driver. If you want to use COPP 
// to enforce video output protection, the application *must* validate 
// the certificate returned by the KeyExchange method. 
// 
// The purpose of this function is only to test whether the driver 
// claims to support COPP. 
//------------------------------------------------------------------------

COPPSupport IsDriverCoppEnabled(const WCHAR *wszTestFile)
{
    COPPSupport SupportResult = CANNOT_DETERMINE_COPP_SUPPORT; 

    IGraphBuilder *pGB = NULL;
    IBaseFilter *pRenderer = NULL;
    IAMCertifiedOutputProtection  *pCOPPDevice = NULL;
    BYTE *pbCertificate = NULL;
    GUID  RandomValue = GUID_NULL;
    ULONG cbCertificateLength = NULL;
    
    HRESULT hr = S_OK;

    CHECK_HR(hr = CoInitializeEx(NULL, COINIT_MULTITHREADED));
   
    // Create the Filter Graph Manager.
    CHECK_HR(hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void**)&pGB));

    // Create the VMR-9. 
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9,
        NULL, CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
        (void**)&pRenderer
        ));

    if (FAILED(hr))
    {
        // Try the VMR-7 instead.
        CHECK_HR(hr = CoCreateInstance(CLSID_VideoMixingRenderer,
                NULL, CLSCTX_INPROC, IID_IBaseFilter, 
                (void**)&pRenderer
                ));
    }

    // Add the VMR to the filter graph.
    CHECK_HR(hr = pGB->AddFilter(pRenderer, L"Video Renderer"));

    // Build a default playback graph.
    CHECK_HR(hr = pGB->RenderFile(wszTestFile, NULL));

    // Query for IAMCertifiedOutputProtection.
    CHECK_HR(hr = pRenderer->QueryInterface(IID_IAMCertifiedOutputProtection,
            (void**)&pCOPPDevice));

    // Get the driver's COPP certificate.
    hr = pCOPPDevice->KeyExchange(&RandomValue, &pbCertificate,
        &cbCertificateLength);

    if (SUCCEEDED(hr))
    {
        SupportResult = SUPPORTS_COPP;
    }
    else
    {
        SupportResult = DOES_NOT_SUPPORT_COPP;
    }

done:
    // Clean up.
    CoTaskMemFree(pbCertificate);
    SAFE_RELEASE(pCOPPDevice);
    SAFE_RELEASE(pRenderer);
    SAFE_RELEASE(pGB);
    CoUninitialize();

    return SupportResult;
} 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Protocolo de Proteção de Saída Certificado](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



