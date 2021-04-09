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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="cbcb1-103">Inserindo um sumário em um arquivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="cbcb1-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="cbcb1-104">Este tópico demonstra como criar um sumário (índice analítico) e incorporá-lo em um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="cbcb1-105">Para manter o código de exemplo curto, o Sumário é muito simples; Ele contém apenas uma entrada e a entrada é populada com um mínimo de informações.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="cbcb1-106">Para criar um sumário e inseri-lo em um arquivo, você deve criar os quatro objetos a seguir chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="cbcb1-107">Entrada de Sumário</span><span class="sxs-lookup"><span data-stu-id="cbcb1-107">TOC Entry</span></span>
-   <span data-ttu-id="cbcb1-108">Lista de entradas de Sumário</span><span class="sxs-lookup"><span data-stu-id="cbcb1-108">TOC Entry List</span></span>
-   <span data-ttu-id="cbcb1-109">SUMÁRIO</span><span class="sxs-lookup"><span data-stu-id="cbcb1-109">TOC</span></span>
-   <span data-ttu-id="cbcb1-110">Analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="cbcb1-110">TOC Parser</span></span>

<span data-ttu-id="cbcb1-111">Identificadores de classe para os objetos são fornecidos em [identificadores de classe para o analisador de](class-identifiers-for-toc-parser.md)Sumário.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="cbcb1-112">Primeiro, preencha a entrada de Sumário com informações que descrevem uma parte do arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="cbcb1-113">Adicione a entrada de Sumário à lista de entradas de Sumário e, em seguida, adicione a lista de entradas de Sumário ao Sumário.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="cbcb1-114">Por fim, adicione o Sumário ao analisador de Sumário, que fornece a funcionalidade para inserir o Sumário no arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="cbcb1-115">A lista a seguir fornece as etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="cbcb1-116">Crie um objeto de entrada de Sumário e obtenha uma interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) nele.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="cbcb1-117">Preencha uma estrutura de [**\_ \_ descritor de entrada de Sumário**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) e passe-a para [**ITocEntry:: setdescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="cbcb1-118">Crie um objeto de lista de entradas de Sumário e obtenha uma interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) nele.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="cbcb1-119">Adicione o objeto de entrada de Sumário criado na etapa 1 ao objeto da lista de entradas de Sumário chamando [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="cbcb1-120">Crie um objeto TOC e obtenha uma interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) nele.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="cbcb1-121">Adicione o objeto de lista de entradas de Sumário criado na etapa 3 ao objeto TOC chamando [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="cbcb1-122">Crie um objeto de analisador de Sumário e obtenha uma interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) nele.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="cbcb1-123">Chame [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar o objeto do analisador de Sumário e associá-lo a um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="cbcb1-124">Adicione o objeto TOC criado na etapa 5 ao objeto analisador de Sumário chamando [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="cbcb1-125">Insira o Sumário no arquivo de vídeo chamando [**ITocParser:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span><span class="sxs-lookup"><span data-stu-id="cbcb1-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="cbcb1-126">O código a seguir demonstra as etapas fornecidas na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="cbcb1-126">The following code demonstrates the steps given in the preceding list.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cbcb1-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbcb1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbcb1-128">Lendo um Sumário de um arquivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="cbcb1-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="cbcb1-129">Objetos do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="cbcb1-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="cbcb1-130">Guia de programação do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="cbcb1-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



