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
# <a name="generating-a-table-of-contents-automatically"></a>Gerando um sumário automaticamente

Este tópico demonstra como usar o componente [**de gerador de**](/previous-versions/ee264297(v=vs.85)) Sumário (gerador de Sumário) para gerar automaticamente um sumário para um arquivo de vídeo.

O gerador de Sumário é um DMO (objeto de mídia do DirectX). Para usar o gerador de Sumário DMO, crie um grafo de filtro DirectX que tenha um arquivo de vídeo como fonte. Insira o TOC Generator DMO no gráfico de filtro e execute o grafo. Em seguida, você pode obter o Sumário gerado automaticamente do gerador de Sumário DMO.

O procedimento a seguir fornece as etapas mais detalhadamente.

1.  Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de filtro de gráfico (**CLSID \_ FilterGraph**) e obtenha uma interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
2.  Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de filtro de invólucro do DMO (**CLSID \_ DMOWrapperFilter**) e obtenha uma interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Passe **\_ CTocGeneratorDmo CLSID** para o método [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) do seu filtro de invólucro do DMO. Isso cria um gerador de Sumário DMO e o encapsula em seu filtro de invólucro do DMO.
4.  Chame o método [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) da interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para adicionar o gerador de Sumário encapsulado DMO ao grafo de filtro.
    > [!Note]  
    > [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) herda de [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).

     

5.  Chame o método [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) da sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) para criar um filtro de recursos e adicioná-lo ao grafo.
6.  Enumere os Pins no filtro de invólucro do DMO e no filtro de origem. Isso envolve a obtenção de interfaces [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) e de interfaces [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) .
7.  Conecte o filtro de origem e o filtro de wrapper chamando o método [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) da sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
8.  Conclua o grafo chamando o método [**render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de sua interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
9.  Execute o grafo ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) e aguarde até que ele seja concluído ([**IMediaEvent:: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).
10. Obtenha uma interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) no seu wrapper de filtro de DMO e obtenha o valor da propriedade [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) . Repita se necessário até que o Sumário esteja pronto.
11. Use a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o valor da propriedade [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) . Essa propriedade é uma interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) que representa o Sumário gerado automaticamente.

O código a seguir demonstra o procedimento para gerar um sumário automaticamente. O código usa três funções auxiliares ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)e [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) que são mostradas em outras páginas desta documentação.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Função BuildGraph para gerar um sumário](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Função GetToc para gerar um sumário](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Função RunGraphAndWait para gerar um sumário](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Guia de programação do analisador de Sumário](toc-parser-programming-guide.md)
</dt> </dl>

 

 
