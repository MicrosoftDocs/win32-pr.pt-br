---
description: Esta seção descreve como enumerar Media Foundation e como registrar um MFT personalizado para que os aplicativos possam descobri-lo.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrando e enumerando MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3110351479f2a906d68b6c054d9e23886cbcd4cdb031fc8a4951a1d4b8d1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101825"
---
# <a name="registering-and-enumerating-mfts"></a>Registrando e enumerando MFTs

Esta seção descreve como enumerar Media Foundation e como registrar um MFT personalizado para que os aplicativos possam descobri-lo.

-   [Enumerando MFTs](#registering-and-enumerating-mfts)
-   [Registrando MFTs](#registering-mfts)
-   [Tópicos relacionados](#related-topics)

## <a name="enumerating-mfts"></a>Enumerando MFTs

Para descobrir MFTs registrados no sistema, um aplicativo pode chamar a [**função MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

> [!Note]  
> Essa função requer a Windows 7. Antes do Windows 7, os aplicativos devem usar a [**função MFTEnum.**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)

 

Essa função recebe as seguintes informações como entrada:

-   A categoria de MFT a ser enumerada, como decodificador de vídeo ou decodificador de áudio.
-   Um formato de entrada ou saída a ser corresponder.
-   Sinalizadores que especificam condições de pesquisa adicionais.

A função retorna uma matriz de [**ponteiros IMFActivate,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) cada um deles representando uma MFT que corresponde aos critérios de enumeração.

Por exemplo, o código a seguir enumera Windows decodificadores de Vídeo de Mídia:


```C++
HRESULT hr = S_OK;
UINT32 count = 0;

IMFActivate **ppActivate = NULL;    // Array of activation objects.
IMFTransform *pDecoder = NULL;      // Pointer to the decoder.

// Match WMV3 video.
MFT_REGISTER_TYPE_INFO info = { MFMediaType_Video, MFVideoFormat_WMV3 };

UINT32 unFlags = MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;

hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );


if (SUCCEEDED(hr) && count == 0)
{
    hr = MF_E_TOPO_CODEC_NOT_FOUND;
}

// Create the first decoder in the list.

if (SUCCEEDED(hr))
{
    hr = ppActivate[0]->ActivateObject(IID_PPV_ARGS(&pDecoder));
}

for (UINT32 i = 0; i < count; i++)
{
    ppActivate[i]->Release();
}
CoTaskMemFree(ppActivate);
```



Por padrão, alguns tipos de MFT são excluídos da enumeração, incluindo MFTs assíncronos, MFTs de hardware e MFTs com reestruturações de campo de uso. Eles são excluídos porque todos exigem tratamento especial de algum tipo. Use o *parâmetro Flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para alterar o padrão. Por exemplo, para incluir MFTs de hardware nos resultados da enumeração, de definido o sinalizador HARDWARE do **\_ \_ \_ SINALIZADOR ENUM MFT:**


```C++
UINT32 unFlags = MFT_ENUM_FLAG_HARDWARE |
                 MFT_ENUM_FLAG_SYNCMFT  | 
                 MFT_ENUM_FLAG_LOCALMFT | 
                 MFT_ENUM_FLAG_SORTANDFILTER;
hr = MFTEnumEx(
    MFT_CATEGORY_VIDEO_DECODER,
    unFlags,
    &info,      // Input type
    NULL,       // Output type
    &ppActivate,
    &count
    );
```



## <a name="registering-mfts"></a>Registrando MFTs

Quando você registra uma Media Foundation (MFT), dois tipos de informações são gravados no Registro:

-   O CLSID do MFT, para que os clientes possam chamar **CoCreateInstance** ou **CoGetClassObject** para criar uma instância do MFT. Essa entrada do Registro segue o formato padrão para fábricas de classes COM. Para obter mais informações, consulte a documentação Windows SDK do Component Object Model (COM).
-   Informações que permitem que um aplicativo enumere MFTs por categoria funcional.

Para criar as entradas de enumeração MFT no Registro, chame a [**função MFTRegister.**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) Você pode incluir as seguintes informações sobre o MFT:

-   A categoria do MFT, como decodificador de vídeo ou codificador de vídeo. Para ver uma lista de categorias, consulte [**MFT \_ CATEGORY**](mft-category.md).
-   Uma lista de formatos de entrada e saída compatíveis com o MFT. Cada formato é definido por um tipo principal e um subtipo. (Para obter informações de formato mais detalhadas, o cliente deve criar o MFT e chamar [**métodos IMFTransform.)**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) O carregador de topologia usa essas informações quando resolve uma topologia parcial.

Para remover as entradas do Registro, chame [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

O código a seguir mostra como registrar um MFT. Este exemplo pressuporá que o MFT é um efeito de vídeo que dá suporte aos mesmos formatos para entrada e saída.


```C++
// CLSID of the MFT.
extern const GUID CLSID_MyVideoEffectMFT;

// DllRegisterServer: Creates the registry entries.
STDAPI DllRegisterServer()
{
    HRESULT hr = S_OK;

    // Array of media types.
    MFT_REGISTER_TYPE_INFO aMediaTypes[] =
    {
        {   MFMediaType_Video, MFVideoFormat_NV12 },
        {   MFMediaType_Video, MFVideoFormat_YUY2 },
        {   MFMediaType_Video, MFVideoFormat_UYVY },
    };

    // Size of the array.
    const DWORD cNumMediaTypes = ARRAY_SIZE(aMediaTypes);

    hr = MFTRegister(
        CLSID_MyVideoEffectMFT,     // CLSID.
        MFT_CATEGORY_VIDEO_EFFECT,  // Category.
        L"My Video Effect",         // Friendly name.
        0,                          // Reserved, must be zero.
        cNumMediaTypes,             // Number of input types.
        aMediaTypes,                // Input types.
        cNumMediaTypes,             // Number of output types.
        aMediaTypes,                // Output types.
        NULL                        // Attributes (optional).
        );

    if (SUCCEEDED(hr))
    {
        // Register the CLSID for CoCreateInstance (not shown).
    }
    return hr;
}

// DllUnregisterServer: Removes the registry entries.
STDAPI DllUnregisterServer()
{
    HRESULT hr = MFTUnregister(CLSID_MyVideoEffectMFT);

    // Unregister the CLSID for CoCreateInstance (not shown).

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de campo de uso](field-of-use-restrictions.md)
</dt> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 



