---
description: Testando se um driver gráfico dá suporte a COPP
ms.assetid: e3e1c795-5cfa-4e4b-86aa-948dd2bf91a4
title: Testando se um driver gráfico dá suporte a COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f98a5bfc3f577d1acb45969ec5d10503ae87b27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757867"
---
# <a name="testing-whether-a-graphics-driver-supports-copp"></a><span data-ttu-id="22c69-103">Testando se um driver gráfico dá suporte a COPP</span><span class="sxs-lookup"><span data-stu-id="22c69-103">Testing Whether a Graphics Driver Supports COPP</span></span>

<span data-ttu-id="22c69-104">O protocolo COPP (certificado de proteção de saída) permite que um aplicativo proteja o conteúdo de vídeo à medida que ele viaja da placa de vídeo para o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22c69-104">Certified Output Protection Protocol (COPP) enables an application to protect video content as it travels from the video card to the display device.</span></span> <span data-ttu-id="22c69-105">Se um driver de gráficos oferecer suporte a COPP, o driver terá uma cadeia de certificados, assinada pela Microsoft, Autenticando o driver.</span><span class="sxs-lookup"><span data-stu-id="22c69-105">If a graphics driver supports COPP, the driver holds a certificate chain, signed by Microsoft, authenticating the driver.</span></span> <span data-ttu-id="22c69-106">Os aplicativos de reprodução que usam COPP para impor a proteção de conteúdo devem validar a cadeia de certificados para garantir que o driver não tenha sido adulterado.</span><span class="sxs-lookup"><span data-stu-id="22c69-106">Playback applications that use COPP to enforce content protection must validate the certificate chain to ensure that the driver has not been tampered with.</span></span>

<span data-ttu-id="22c69-107">No entanto, talvez você queira verificar se um driver de gráficos dá suporte a COPP, sem validar o certificado.</span><span class="sxs-lookup"><span data-stu-id="22c69-107">However, you might want to check whether a graphics driver supports COPP, without validating the certificate.</span></span> <span data-ttu-id="22c69-108">Por exemplo, quando um provedor de mídia digital emite uma licença de DRM (gerenciamento de direitos digitais), talvez queira verificar se o usuário tem um driver de gráficos habilitado para COPP.</span><span class="sxs-lookup"><span data-stu-id="22c69-108">For example, when a digital media provider issues a digital rights management (DRM) license, it might want to check whether the user has a COPP-enabled graphics driver.</span></span> <span data-ttu-id="22c69-109">O provedor não precisa impor COPP no momento em que emite a licença; Ele só precisa testar se o driver dá suporte a COPP.</span><span class="sxs-lookup"><span data-stu-id="22c69-109">The provider does not need to enforce COPP at the time it issues the license; it only needs to test whether the driver supports COPP.</span></span>

<span data-ttu-id="22c69-110">O código a seguir mostra como testar se um driver dá suporte a COPP.</span><span class="sxs-lookup"><span data-stu-id="22c69-110">The following code shows how to test whether a driver supports COPP.</span></span> <span data-ttu-id="22c69-111">O aplicativo deve passar o nome de um arquivo de vídeo que será usado para testar o driver.</span><span class="sxs-lookup"><span data-stu-id="22c69-111">The application must pass in the name of a video file that will be used to test the driver.</span></span> <span data-ttu-id="22c69-112">Isso é necessário porque o filtro de processador de mixagem de vídeo no Microsoft® DirectShow® não Inicializa uma sessão COPP até que o filtro seja conectado.</span><span class="sxs-lookup"><span data-stu-id="22c69-112">This is required because the Video Mixing Renderer filter in Microsoft® DirectShow® does not initialize a COPP session until the filter is connected.</span></span> <span data-ttu-id="22c69-113">Essa função pode ser incluída em um aplicativo cliente para verificar se o driver é capaz de executar a COPP.</span><span class="sxs-lookup"><span data-stu-id="22c69-113">This function can be included in a client application to check if the driver is capable of running COPP.</span></span>

> [!Note]  
> <span data-ttu-id="22c69-114">Se o computador do usuário tiver duas placas gráficas, essa função testará o driver para a placa gráfica primária, mas não a placa gráfica secundária.</span><span class="sxs-lookup"><span data-stu-id="22c69-114">If the user's computer has two graphics cards, this function tests the driver for the primary graphics card, but not the secondary graphics card.</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="22c69-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22c69-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c69-116">Usando o protocolo de proteção de saída certificado</span><span class="sxs-lookup"><span data-stu-id="22c69-116">Using Certified Output Protection Protocol</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



