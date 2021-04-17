---
description: Usando o Windows Media com os serviços de edição do DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Usando o Windows Media com os serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789676"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="38d64-103">Usando o Windows Media com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="38d64-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="38d64-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="38d64-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="38d64-105">Esta seção descreve como usar o conteúdo baseado no Windows Media em um aplicativo de [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="38d64-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="38d64-106">Há dois cenários principais:</span><span class="sxs-lookup"><span data-stu-id="38d64-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="38d64-107">Clipes de origem.</span><span class="sxs-lookup"><span data-stu-id="38d64-107">Source clips.</span></span> <span data-ttu-id="38d64-108">Um projeto DES pode conter clipes de áudio e vídeo de arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="38d64-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="38d64-109">Formato de destino.</span><span class="sxs-lookup"><span data-stu-id="38d64-109">Target format.</span></span> <span data-ttu-id="38d64-110">O Windows Media é um formato ideal para a saída final de um projeto de edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="38d64-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="38d64-111">Para trabalhar com arquivos de mídia do Windows, o aplicativo deve fornecer um certificado de software, também chamado de chave.</span><span class="sxs-lookup"><span data-stu-id="38d64-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="38d64-112">Ele faz isso implementando um objeto de provedor de chave.</span><span class="sxs-lookup"><span data-stu-id="38d64-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="38d64-113">O provedor de chave é um objeto COM que expõe a interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="38d64-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="38d64-114">Para obter informações sobre como implementar o provedor de chaves, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="38d64-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="38d64-115">Para usar DES com arquivos de mídia do Windows, os seguintes objetos DES requerem a chave de software:</span><span class="sxs-lookup"><span data-stu-id="38d64-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="38d64-116">O mecanismo de renderização, para visualização ou gravação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="38d64-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="38d64-117">O objeto MediaDet, para obter quadros de vídeo ou tipos de mídia de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="38d64-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="38d64-118">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="38d64-118">\[!Important\]</span></span>  
    > <span data-ttu-id="38d64-119">Não use o mecanismo de processamento inteligente para ler ou gravar arquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="38d64-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="38d64-120">Sempre use o mecanismo de processamento básico (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="38d64-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="38d64-121">Para dar a um objeto a chave de software, consulte esse objeto para a interface **IObjectWithSite** e chame **IObjectWithSite:: SetSite** com um ponteiro para o provedor de chave.</span><span class="sxs-lookup"><span data-stu-id="38d64-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="38d64-122">Por exemplo, o código a seguir fornece a chave de software para o mecanismo de renderização:</span><span class="sxs-lookup"><span data-stu-id="38d64-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="38d64-123">Para usar os clipes de origem do Windows Media em um projeto DES, basta chamar **IObjectWithSite:: SetSite** no mecanismo de renderização com um ponteiro para o provedor de chave.</span><span class="sxs-lookup"><span data-stu-id="38d64-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="38d64-124">Para obter informações sobre como gravar arquivos de mídia do Windows, consulte [gravando um arquivo de mídia do Windows em des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="38d64-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="38d64-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38d64-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38d64-126">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="38d64-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



