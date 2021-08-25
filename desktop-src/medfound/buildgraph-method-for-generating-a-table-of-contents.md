---
description: Função BuildGraph para gerar um tabela de conteúdo
ms.assetid: f70740ef-4c58-4944-9be6-dd056e12ad93
title: Função BuildGraph para gerar um tabela de conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2346676eb868fb4d1a2cc30ebebdec9ec63f1a80858203729315d1019f7cd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959505"
---
# <a name="buildgraph-function-for-generating-a-table-of-contents"></a>Função BuildGraph para gerar um tabela de conteúdo

A função a seguir é uma função auxiliar em um programa de exemplo que é discutido em Gerando um [tabela de conteúdo automaticamente.](generating-a-table-of-contents-automatically.md)


```C++
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap)
{
   IBaseFilter* pTocGeneratorBase = NULL;
   HRESULT hr = pWrap->QueryInterface(IID_IBaseFilter, (VOID**)&pTocGeneratorBase);

   if(SUCCEEDED(hr))
   {
      hr = pGraph->AddFilter(pTocGeneratorBase, L"TOC Generator");

      if(SUCCEEDED(hr))
      {
         IBaseFilter* pSourceBase = NULL;
         hr = pGraph->AddSourceFilter(g_sourceFile, L"Source", &pSourceBase);

         if(SUCCEEDED(hr))
         { 
            IEnumPins* pTocGenPins = NULL;
            hr = pTocGeneratorBase->EnumPins(&pTocGenPins);

            if(SUCCEEDED(hr))
            {                            
               ULONG numPins = 0;
               IPin* pTocGenInput = NULL;  // 1st pin is input.
               hr = pTocGenPins->Next(1, &pTocGenInput, &numPins);

               if(SUCCEEDED(hr))
               {                           
                  numPins = 0;
                  IPin* pTocGenOutput = NULL;  // 2nd pin is output.
                  hr = pTocGenPins->Next(1, &pTocGenOutput, &numPins);

                  if(SUCCEEDED(hr))
                  {
                     IEnumPins* pSourcePins = NULL;
                     hr = pSourceBase->EnumPins(&pSourcePins);

                     if(SUCCEEDED(hr))
                     {
                        numPins = 0;
                        IPin* pSourceInput = NULL;
                        hr = pSourcePins->Next(1, &pSourceInput, &numPins);
                      
                        // We don't need the first pin, so discard it.
                        if(NULL != pSourceInput)
                        {
                           pSourceInput->Release();
                           pSourceInput = NULL;
                        }

                        IPin* pSourceOutput = NULL;  // 2nd pin is output.
                        hr = pSourcePins->Next(1, &pSourceOutput, &numPins);

                        if(SUCCEEDED(hr))
                        { 
                           hr = pGraph->Connect(pSourceOutput, pTocGenInput);

                           if(SUCCEEDED(hr))
                           {
                              hr = pGraph->Render(pTocGenOutput);
                           }

                           pSourceOutput->Release();
                           pSourceOutput = NULL;
                        }

                        pSourcePins->Release();
                        pSourcePins = NULL;
                     }

                     pTocGenOutput->Release();
                     pTocGenOutput = NULL;
                  }

                  pTocGenInput->Release();
                  pTocGenInput = NULL;
               }

               pTocGenPins->Release();
               pTocGenPins = NULL;
            }
                                               
            pSourceBase->Release();
            pSourceBase = NULL;
         }
      }

      pTocGeneratorBase->Release();
      pTocGeneratorBase = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerando um tabela de conteúdo automaticamente](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



