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
# <a name="registering-and-enumerating-mfts"></a><span data-ttu-id="96c7f-103">Registrando e enumerando MFTs</span><span class="sxs-lookup"><span data-stu-id="96c7f-103">Registering and Enumerating MFTs</span></span>

<span data-ttu-id="96c7f-104">Esta seção descreve como enumerar transformações de Media Foundation e como registrar um MFT personalizado para que os aplicativos possam descobri-lo.</span><span class="sxs-lookup"><span data-stu-id="96c7f-104">This section describes how to enumerate Media Foundation transforms, and how to register a custom MFT so that applications can discover it.</span></span>

-   [<span data-ttu-id="96c7f-105">Enumerando MFTs</span><span class="sxs-lookup"><span data-stu-id="96c7f-105">Enumerating MFTs</span></span>](#registering-and-enumerating-mfts)
-   [<span data-ttu-id="96c7f-106">Registrando MFTs</span><span class="sxs-lookup"><span data-stu-id="96c7f-106">Registering MFTs</span></span>](#registering-mfts)
-   [<span data-ttu-id="96c7f-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96c7f-107">Related topics</span></span>](#related-topics)

## <a name="enumerating-mfts"></a><span data-ttu-id="96c7f-108">Enumerando MFTs</span><span class="sxs-lookup"><span data-stu-id="96c7f-108">Enumerating MFTs</span></span>

<span data-ttu-id="96c7f-109">Para descobrir MFTs que estão registrados no sistema, um aplicativo pode chamar a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="96c7f-109">To discover MFTs that are registered on the system, an application can call the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

> [!Note]  
> <span data-ttu-id="96c7f-110">Essa função requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="96c7f-110">This function requires to Windows 7.</span></span> <span data-ttu-id="96c7f-111">Antes do Windows 7, os aplicativos devem usar a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="96c7f-111">Prior to Windows 7, applications should use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function instead.</span></span>

 

<span data-ttu-id="96c7f-112">Essa função usa as seguintes informações como entrada:</span><span class="sxs-lookup"><span data-stu-id="96c7f-112">This function takes the following information as input:</span></span>

-   <span data-ttu-id="96c7f-113">A categoria do MFT a ser enumerada, como um decodificador de vídeo ou decodificador de áudio.</span><span class="sxs-lookup"><span data-stu-id="96c7f-113">The category of MFT to enumerate, such as video decoder or audio decoder.</span></span>
-   <span data-ttu-id="96c7f-114">Um formato de entrada ou saída para corresponder.</span><span class="sxs-lookup"><span data-stu-id="96c7f-114">An input or output format to match.</span></span>
-   <span data-ttu-id="96c7f-115">Sinalizadores que especificam critérios de pesquisa adicionais.</span><span class="sxs-lookup"><span data-stu-id="96c7f-115">Flags that specify additional search conditions.</span></span>

<span data-ttu-id="96c7f-116">A função retorna uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada uma representando um MFT que corresponde aos critérios de enumeração.</span><span class="sxs-lookup"><span data-stu-id="96c7f-116">The function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each of which represents an MFT that matches the enumeration criteria.</span></span>

<span data-ttu-id="96c7f-117">Por exemplo, o código a seguir enumera os decodificadores de vídeo do Windows Media:</span><span class="sxs-lookup"><span data-stu-id="96c7f-117">For example, the following code enumerates Windows Media Video decoders:</span></span>


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



<span data-ttu-id="96c7f-118">Por padrão, alguns tipos de MFT são excluídos da enumeração, incluindo MFTs assíncrona, MFTs de hardware e MFTs com restructos de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="96c7f-118">By default, some types of MFT are excluded from the enumeration, including asynchronous MFTs, hardware MFTs, and MFTs with field-of-use restructions.</span></span> <span data-ttu-id="96c7f-119">Eles são excluídos porque todos exigem tratamento especial de algum tipo.</span><span class="sxs-lookup"><span data-stu-id="96c7f-119">These are excluded because they all require special handling of some kind.</span></span> <span data-ttu-id="96c7f-120">Use o parâmetro *flags* de [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para alterar o padrão.</span><span class="sxs-lookup"><span data-stu-id="96c7f-120">Use the *Flags* parameter of [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) to change the default.</span></span> <span data-ttu-id="96c7f-121">Por exemplo, para incluir MFTs de hardware nos resultados da enumeração, defina o sinalizador de **enumeração do sinalizador de enum do MFT \_ \_ \_** :</span><span class="sxs-lookup"><span data-stu-id="96c7f-121">For example, to include hardware MFTs in the enumeration results, set the **MFT\_ENUM\_FLAG\_HARDWARE** flag:</span></span>


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



## <a name="registering-mfts"></a><span data-ttu-id="96c7f-122">Registrando MFTs</span><span class="sxs-lookup"><span data-stu-id="96c7f-122">Registering MFTs</span></span>

<span data-ttu-id="96c7f-123">Quando você registra uma Media Foundation transformação (MFT), dois tipos de informações são gravados no registro:</span><span class="sxs-lookup"><span data-stu-id="96c7f-123">When you register a Media Foundation transform (MFT), two types of information are written to the registry:</span></span>

-   <span data-ttu-id="96c7f-124">O CLSID do MFT, para que os clientes possam chamar **CoCreateInstance** ou **CoGetClassObject** para criar uma instância do MFT.</span><span class="sxs-lookup"><span data-stu-id="96c7f-124">The CLSID of the MFT, so that clients can call **CoCreateInstance** or **CoGetClassObject** to create an instance of the MFT.</span></span> <span data-ttu-id="96c7f-125">Essa entrada de registro segue o formato padrão para fábricas de classes COM.</span><span class="sxs-lookup"><span data-stu-id="96c7f-125">This registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="96c7f-126">Para obter mais informações, consulte a documentação do SDK do Windows para o Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="96c7f-126">For more information, see the Windows SDK documentation for the Component Object Model (COM).</span></span>
-   <span data-ttu-id="96c7f-127">Informações que permitem que um aplicativo enumere MFTs por categoria funcional.</span><span class="sxs-lookup"><span data-stu-id="96c7f-127">Information that enables an application to enumerate MFTs by functional category.</span></span>

<span data-ttu-id="96c7f-128">Para criar as entradas de enumeração de MFT no registro, chame a função [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) .</span><span class="sxs-lookup"><span data-stu-id="96c7f-128">To create the MFT enumeration entries in the registry, call the [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) function.</span></span> <span data-ttu-id="96c7f-129">Você pode incluir as seguintes informações sobre o MFT:</span><span class="sxs-lookup"><span data-stu-id="96c7f-129">You can include the following information about the MFT:</span></span>

-   <span data-ttu-id="96c7f-130">A categoria do MFT, como um decodificador de vídeo ou codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="96c7f-130">The category of the MFT, such as video decoder or video encoder.</span></span> <span data-ttu-id="96c7f-131">Para obter uma lista de categorias, consulte a [**\_ categoria MFT**](mft-category.md).</span><span class="sxs-lookup"><span data-stu-id="96c7f-131">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>
-   <span data-ttu-id="96c7f-132">Uma lista de formatos de entrada e saída para os quais a MFT dá suporte.</span><span class="sxs-lookup"><span data-stu-id="96c7f-132">A list of input and output formats that the MFT supports.</span></span> <span data-ttu-id="96c7f-133">Cada formato é definido por um tipo principal e um subtipo.</span><span class="sxs-lookup"><span data-stu-id="96c7f-133">Each format is defined by a major type and a subtype.</span></span> <span data-ttu-id="96c7f-134">(Para obter informações de formato mais detalhadas, o cliente deve criar a MFT e chamar os métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .) O carregador de topologia usa essas informações quando resolve uma topologia parcial.</span><span class="sxs-lookup"><span data-stu-id="96c7f-134">(To get more detailed format information, the client must create the MFT and call [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods.) The topology loader uses this information when it resolves a partial topology.</span></span>

<span data-ttu-id="96c7f-135">Para remover as entradas do registro, chame [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span><span class="sxs-lookup"><span data-stu-id="96c7f-135">To remove the entries from the registry, call [**MFTUnregister**](/windows/desktop/api/mfapi/nf-mfapi-mftunregister).</span></span>

<span data-ttu-id="96c7f-136">O código a seguir mostra como registrar um MFT.</span><span class="sxs-lookup"><span data-stu-id="96c7f-136">The following code shows how to register an MFT.</span></span> <span data-ttu-id="96c7f-137">Este exemplo pressupõe que o MFT é um efeito de vídeo que dá suporte aos mesmos formatos para entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="96c7f-137">This example assumes that the MFT is a video effect that supports the same formats for both input and output.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="96c7f-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96c7f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96c7f-139">Campo de restrições de uso</span><span class="sxs-lookup"><span data-stu-id="96c7f-139">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="96c7f-140">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96c7f-140">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 



