---
description: Criando o objeto divisor de ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Criando o objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826736"
---
# <a name="creating-the-asf-splitter-object"></a><span data-ttu-id="60655-103">Criando o objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="60655-103">Creating the ASF Splitter Object</span></span>

<span data-ttu-id="60655-104">O objeto *divisor* de ASF é um objeto de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="60655-104">The ASF *splitter* object is a WMContainer layer object that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="60655-105">Para criar uma nova instância do objeto divisor de ASF, chame a função [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="60655-105">To create a new instance of the ASF splitter object, call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function.</span></span> <span data-ttu-id="60655-106">Essa função retorna um ponteiro para a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) que representa um objeto divisor vazio.</span><span class="sxs-lookup"><span data-stu-id="60655-106">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface that represents an empty splitter object.</span></span>

<span data-ttu-id="60655-107">Antes que o divisor possa começar a análise, o aplicativo deve inicializar o separador com informações do objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="60655-107">Before the splitter can begin parsing, the application must initialize the splitter with information from the ASF Header Object.</span></span> <span data-ttu-id="60655-108">Para inicializar o divisor, chame o método [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="60655-108">To initialize the splitter, call the [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) method.</span></span> <span data-ttu-id="60655-109">Esse método usa um ponteiro para o [objeto ContentInfo do ASF](asf-contentinfo-object.md) que contém informações de cabeçalho do arquivo ASF a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="60655-109">This method takes a pointer to the [ASF ContentInfo Object](asf-contentinfo-object.md) that contains header information of the ASF file to parse.</span></span> <span data-ttu-id="60655-110">O aplicativo deve inicializar o objeto ContentInfo antes de passá-lo para o divisor para que as características do arquivo de mídia sejam conhecidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60655-110">The application must initialize the ContentInfo object before passing it to the splitter so that the characteristics of the media file are known to the application.</span></span> <span data-ttu-id="60655-111">O método **Initialize** do separador extrai informações de fluxo do objeto ContentInfo, como números de fluxo, para que o divisor possa analisar os pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="60655-111">The splitter's **Initialize** method extracts stream information from the ContentInfo object, such as stream numbers, so the splitter can parse the data packets.</span></span>

### <a name="example"></a><span data-ttu-id="60655-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="60655-112">Example</span></span>

<span data-ttu-id="60655-113">O exemplo de código a seguir mostra como criar um divisor e inicializá-lo com um objeto ContentInfo existente.</span><span class="sxs-lookup"><span data-stu-id="60655-113">The following code example shows how to create a splitter and initialize it with an existing ContentInfo object.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="60655-114">Este exemplo usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="60655-114">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="60655-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60655-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60655-116">Divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="60655-116">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



