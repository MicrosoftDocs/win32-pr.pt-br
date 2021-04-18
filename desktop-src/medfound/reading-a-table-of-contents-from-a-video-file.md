---
description: Lendo um Sumário de um arquivo de vídeo
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lendo um Sumário de um arquivo de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788699"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a><span data-ttu-id="3bb48-103">Lendo um Sumário de um arquivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="3bb48-103">Reading a Table of Contents from a Video File</span></span>

<span data-ttu-id="3bb48-104">Este tópico demonstra como ler um sumário que já foi inserido em um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3bb48-104">This topic demonstrates how to read a table of contents that has already been embedded in a video file.</span></span>

<span data-ttu-id="3bb48-105">Comece chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de analisador de Sumário e obter uma interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .</span><span class="sxs-lookup"><span data-stu-id="3bb48-105">Start by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface.</span></span> <span data-ttu-id="3bb48-106">Em seguida, obtenha as seguintes interfaces chamando métodos.</span><span class="sxs-lookup"><span data-stu-id="3bb48-106">Then obtain the following interfaces by calling methods.</span></span>

-   [<span data-ttu-id="3bb48-107">**IToc**</span><span class="sxs-lookup"><span data-stu-id="3bb48-107">**IToc**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [<span data-ttu-id="3bb48-108">**ITocEntryList**</span><span class="sxs-lookup"><span data-stu-id="3bb48-108">**ITocEntryList**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [<span data-ttu-id="3bb48-109">**ITocEntry**</span><span class="sxs-lookup"><span data-stu-id="3bb48-109">**ITocEntry**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

<span data-ttu-id="3bb48-110">Use os métodos de [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) para inspecionar uma entrada individual no sumário.</span><span class="sxs-lookup"><span data-stu-id="3bb48-110">Use the methods of [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) to inspect an individual entry in the table of contents.</span></span> <span data-ttu-id="3bb48-111">Por exemplo, você pode inspecionar o título, a hora de início e a hora de término da entrada.</span><span class="sxs-lookup"><span data-stu-id="3bb48-111">For example, you can inspect the title, the start time, and the end time of the entry.</span></span>

<span data-ttu-id="3bb48-112">A lista a seguir fornece as etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="3bb48-112">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="3bb48-113">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um objeto de analisador de Sumário e obtenha uma interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) nele.</span><span class="sxs-lookup"><span data-stu-id="3bb48-113">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
2.  <span data-ttu-id="3bb48-114">Chame [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) para inicializar o analisador de Sumário e associá-lo a um arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3bb48-114">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC parser and associate it with a video file.</span></span>
3.  <span data-ttu-id="3bb48-115">Obtenha uma interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) chamando [**ITocParser:: GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span><span class="sxs-lookup"><span data-stu-id="3bb48-115">Obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface by calling [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span></span>
4.  <span data-ttu-id="3bb48-116">Obtenha uma interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) chamando [**IToc:: GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="3bb48-116">Obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface by calling [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span></span>
5.  <span data-ttu-id="3bb48-117">Obtenha uma interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) chamando [**ITocEntryList:: GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="3bb48-117">Obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface by calling [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span></span>
6.  <span data-ttu-id="3bb48-118">Aloque uma estrutura de [**\_ \_ descritor de entrada de Sumário**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="3bb48-118">Allocate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure.</span></span>
7.  <span data-ttu-id="3bb48-119">Preencha a estrutura do [**\_ \_ descritor de entrada de Sumário**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) chamando [**ITocEntry:: getdescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span><span class="sxs-lookup"><span data-stu-id="3bb48-119">Populate the [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure by calling [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span></span>

<span data-ttu-id="3bb48-120">O código a seguir demonstra as etapas na lista anterior.</span><span class="sxs-lookup"><span data-stu-id="3bb48-120">The following code demonstrates the steps in the preceding list.</span></span>


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3bb48-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bb48-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bb48-122">Inserindo um sumário em um arquivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="3bb48-122">Embedding a Table of Contents in a Video File</span></span>](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="3bb48-123">Objetos do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="3bb48-123">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="3bb48-124">Guia de programação do analisador de Sumário</span><span class="sxs-lookup"><span data-stu-id="3bb48-124">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
