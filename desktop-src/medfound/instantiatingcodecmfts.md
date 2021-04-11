---
description: Criando uma instância do codec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Criando uma instância do codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164572"
---
# <a name="instantiating-codec-mfts"></a><span data-ttu-id="cd5aa-103">Criando uma instância do codec MFTs</span><span class="sxs-lookup"><span data-stu-id="cd5aa-103">Instantiating Codec MFTs</span></span>

<span data-ttu-id="cd5aa-104">[Media Foundation transformações](media-foundation-transforms.md) (MFTs) são objetos com que implementam a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="cd5aa-104">[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) are COM objects that implement the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="cd5aa-105">Um MFT é um objeto para transformar dados de multimídia como parte de um pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-105">An MFT is an object for transforming multimedia data as part of a pipeline.</span></span> <span data-ttu-id="cd5aa-106">Um pipeline é um grafo acíclico direcionado, que consiste em fontes de mídia, transformações de mídia e coletores de mídia.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-106">A pipeline is a directed acyclic graph, consisting of media sources, media transforms, and media sinks.</span></span> <span data-ttu-id="cd5aa-107">Um pipeline processa o streaming de dados de multimídia de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-107">A pipeline processes streaming multimedia data asynchronously.</span></span>

<span data-ttu-id="cd5aa-108">Embora MFTs possa ser instanciado e usado independentemente da infraestrutura de pipeline Media Foundation, é preferível usar a estrutura MediaFoundation sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-108">Although MFTs can be instantiated and used independently of the Media Foundation pipeline infrastructure, it is preferable to use the MediaFoundation framework where possible.</span></span>

<span data-ttu-id="cd5aa-109">Você pode criar um MFT de codec chamando a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="cd5aa-109">You can create a codec MFT by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="cd5aa-110">Você deve passar o identificador de classe do MFT, o identificador de interface de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)e um ponteiro para um ponteiro **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="cd5aa-110">You must pass the class identifier of the MFT, the interface identifier of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), and a pointer to an **IMFTransform** pointer.</span></span>

<span data-ttu-id="cd5aa-111">Os identificadores de classe do codec MFTs são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-111">The class identifiers of the codec MFTs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="cd5aa-112">A constante para o identificador de interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) é \_ IMFTransform de IID.</span><span class="sxs-lookup"><span data-stu-id="cd5aa-112">The constant for the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface identifier is IID\_IMFTransform.</span></span>

<span data-ttu-id="cd5aa-113">O exemplo de código a seguir demonstra como criar uma instância de um MFT do Codec:</span><span class="sxs-lookup"><span data-stu-id="cd5aa-113">The following code example demonstrates how to create an instance of a codec MFT:</span></span>


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a><span data-ttu-id="cd5aa-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd5aa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd5aa-115">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="cd5aa-115">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 
