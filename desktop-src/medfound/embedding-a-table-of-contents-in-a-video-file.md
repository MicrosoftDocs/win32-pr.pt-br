---
description: Inserindo um sumário em um arquivo de vídeo
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Inserindo um sumário em um arquivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089744"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Inserindo um sumário em um arquivo de vídeo

Este tópico demonstra como criar um sumário (índice analítico) e incorporá-lo em um arquivo de vídeo. Para manter o código de exemplo curto, o Sumário é muito simples; Ele contém apenas uma entrada e a entrada é populada com um mínimo de informações.

Para criar um sumário e inseri-lo em um arquivo, você deve criar os quatro objetos a seguir chamando **CoCreateInstance**.

-   Entrada de Sumário
-   Lista de entradas de Sumário
-   SUMÁRIO
-   Analisador de Sumário

Identificadores de classe para os objetos são fornecidos em [identificadores de classe para o analisador de](class-identifiers-for-toc-parser.md)Sumário.

Primeiro, preencha a entrada de Sumário com informações que descrevem uma parte do arquivo de vídeo. Adicione a entrada de Sumário à lista de entradas de Sumário e, em seguida, adicione a lista de entradas de Sumário ao Sumário. Por fim, adicione o Sumário ao analisador de Sumário, que fornece a funcionalidade para inserir o Sumário no arquivo de vídeo. A lista a seguir fornece as etapas mais detalhadamente.

1.  Crie um objeto de entrada de Sumário e obtenha uma interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) nele.
2.  Preencha uma estrutura de [**\_ \_ descritor de entrada de Sumário**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) e passe-a para [**ITocEntry:: setdescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Crie um objeto de lista de entradas de Sumário e obtenha uma interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) nele.
4.  Adicione o objeto de entrada de Sumário criado na etapa 1 ao objeto da lista de entradas de Sumário chamando [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).
5.  Crie um objeto TOC e obtenha uma interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) nele.
6.  Adicione o objeto de lista de entradas de Sumário criado na etapa 3 ao objeto TOC chamando [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).
7.  Crie um objeto de analisador de Sumário e obtenha uma interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) nele.
8.  Chame [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar o objeto do analisador de Sumário e associá-lo a um arquivo de vídeo.
9.  Adicione o objeto TOC criado na etapa 5 ao objeto analisador de Sumário chamando [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).
10. Insira o Sumário no arquivo de vídeo chamando [**ITocParser:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).

O código a seguir demonstra as etapas fornecidas na lista anterior.


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo um Sumário de um arquivo de vídeo](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Objetos do analisador de Sumário](toc-parser-objects.md)
</dt> <dt>

[Guia de programação do analisador de Sumário](toc-parser-programming-guide.md)
</dt> </dl>

 

 



