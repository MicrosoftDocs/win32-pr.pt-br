---
description: Esta seção descreve como enumerar transformações de Media Foundation e como registrar um MFT personalizado para que os aplicativos possam descobri-lo.
ms.assetid: 76d2a703-4162-428e-a4ff-643e346eacfb
title: Registrando e enumerando MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a22b469d472dbc59d07c2754405276883bef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921210"
---
# <a name="registering-and-enumerating-mfts"></a>Registrando e enumerando MFTs

Esta seção descreve como enumerar transformações de Media Foundation e como registrar um MFT personalizado para que os aplicativos possam descobri-lo.

-   [Enumerando MFTs](#registering-and-enumerating-mfts)
-   [Registrando MFTs](#registering-mfts)
-   [Tópicos relacionados](#related-topics)

## <a name="enumerating-mfts"></a>Enumerando MFTs

Para descobrir MFTs que estão registrados no sistema, um aplicativo pode chamar a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

> [!Note]  
> Essa função requer o Windows 7. Antes do Windows 7, os aplicativos devem usar a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) em vez disso.

 

Essa função usa as seguintes informações como entrada:

-   A categoria do MFT a ser enumerada, como um decodificador de vídeo ou decodificador de áudio.
-   Um formato de entrada ou saída para corresponder.
-   Sinalizadores que especificam critérios de pesquisa adicionais.

A função retorna uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uma representando um MFT que corresponde aos critérios de enumeração.

Por exemplo, o código a seguir enumera os decodificadores de vídeo do Windows Media:


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



Por padrão, alguns tipos de MFT são excluídos da enumeração, incluindo MFTs assíncrona, MFTs de hardware e MFTs com restructos de campo de uso. Eles são excluídos porque todos exigem tratamento especial de algum tipo. Use o parâmetro *flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para alterar o padrão. Por exemplo, para incluir MFTs de hardware nos resultados da enumeração, defina o sinalizador de **enumeração do sinalizador de enum do MFT \_ \_ \_** :


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

Quando você registra uma Media Foundation transformação (MFT), dois tipos de informações são gravados no registro:

-   O CLSID do MFT, para que os clientes possam chamar **CoCreateInstance** ou **CoGetClassObject** para criar uma instância do MFT. Essa entrada de registro segue o formato padrão para fábricas de classes COM. Para obter mais informações, consulte a documentação do SDK do Windows para o Component Object Model (COM).
-   Informações que permitem que um aplicativo enumere MFTs por categoria funcional.

Para criar as entradas de enumeração de MFT no registro, chame a função [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) . Você pode incluir as seguintes informações sobre o MFT:

-   A categoria do MFT, como um decodificador de vídeo ou codificador de vídeo. Para obter uma lista de categorias, consulte a [**\_ categoria MFT**](mft-category.md).
-   Uma lista de formatos de entrada e saída para os quais a MFT dá suporte. Cada formato é definido por um tipo principal e um subtipo. (Para obter informações de formato mais detalhadas, o cliente deve criar a MFT e chamar os métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) O carregador de topologia usa essas informações quando resolve uma topologia parcial.

Para remover as entradas do registro, chame [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).

O código a seguir mostra como registrar um MFT. Este exemplo pressupõe que o MFT é um efeito de vídeo que dá suporte aos mesmos formatos para entrada e saída.


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

[Campo de restrições de uso](field-of-use-restrictions.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



