---
description: Gerando um sumário automaticamente
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Gerando um sumário automaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797963"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="8e61f-103">Gerando um sumário automaticamente</span><span class="sxs-lookup"><span data-stu-id="8e61f-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="8e61f-104">Este tópico demonstra como usar o componente [**de gerador de**](/previous-versions/ee264297(v=vs.85)) Sumário (gerador de Sumário) para gerar automaticamente um sumário para um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8e61f-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="8e61f-105">O gerador de Sumário é um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="8e61f-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="8e61f-106">Para usar o gerador de Sumário DMO, crie um grafo de filtro DirectX que tenha um arquivo de vídeo como fonte.</span><span class="sxs-lookup"><span data-stu-id="8e61f-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="8e61f-107">Insira o TOC Generator DMO no gráfico de filtro e execute o grafo.</span><span class="sxs-lookup"><span data-stu-id="8e61f-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="8e61f-108">Em seguida, você pode obter o Sumário gerado automaticamente do gerador de Sumário DMO.</span><span class="sxs-lookup"><span data-stu-id="8e61f-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="8e61f-109">O procedimento a seguir fornece as etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="8e61f-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="8e61f-110">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de filtro de gráfico (**CLSID \_ FilterGraph**) e obtenha uma interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="8e61f-111">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de filtro de invólucro do DMO (**CLSID \_ DMOWrapperFilter**) e obtenha uma interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="8e61f-112">Passe **\_ CTocGeneratorDmo CLSID** para o método [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) do seu filtro de invólucro do DMO.</span><span class="sxs-lookup"><span data-stu-id="8e61f-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="8e61f-113">Isso cria um gerador de Sumário DMO e o encapsula em seu filtro de invólucro do DMO.</span><span class="sxs-lookup"><span data-stu-id="8e61f-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="8e61f-114">Chame o método [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) da interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para adicionar o gerador de Sumário encapsulado DMO ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="8e61f-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="8e61f-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) herda de [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="8e61f-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="8e61f-116">Chame o método [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) da sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para criar um filtro de recursos e adicioná-lo ao grafo.</span><span class="sxs-lookup"><span data-stu-id="8e61f-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="8e61f-117">Enumere os Pins no filtro de invólucro do DMO e no filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="8e61f-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="8e61f-118">Isso envolve a obtenção de interfaces [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) e de interfaces [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="8e61f-119">Conecte o filtro de origem e o filtro de wrapper chamando o método [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) da sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="8e61f-120">Conclua o grafo chamando o método [**render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="8e61f-121">Execute o grafo ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) e aguarde até que ele seja concluído ([**IMediaEvent:: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="8e61f-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="8e61f-122">Obtenha uma interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) no seu wrapper de filtro de DMO e obtenha o valor da propriedade [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="8e61f-123">Repita se necessário até que o Sumário esteja pronto.</span><span class="sxs-lookup"><span data-stu-id="8e61f-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="8e61f-124">Use a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o valor da propriedade [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e61f-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="8e61f-125">Essa propriedade é uma interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) que representa o Sumário gerado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8e61f-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="8e61f-126">O código a seguir demonstra o procedimento para gerar um sumário automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8e61f-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="8e61f-127">O código usa três funções auxiliares ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)e [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) que são mostradas em outras páginas desta documentação.</span><span class="sxs-lookup"><span data-stu-id="8e61f-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a><span data-ttu-id="8e61f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e61f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e61f-129">Função BuildGraph para gerar um sumário</span><span class="sxs-lookup"><span data-stu-id="8e61f-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8e61f-130">Função GetToc para gerar um sumário</span><span class="sxs-lookup"><span data-stu-id="8e61f-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8e61f-131">Função RunGraphAndWait para gerar um sumário</span><span class="sxs-lookup"><span data-stu-id="8e61f-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8e61f-132">Guia de programação do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="8e61f-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
