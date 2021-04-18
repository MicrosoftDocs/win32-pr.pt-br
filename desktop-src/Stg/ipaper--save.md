---
title: IPaper salvar
description: O foco principal neste código de exemplo é como o copapel pode carregar e salvar seus dados de papel em arquivos compostos. As implementações do método IPaper, Load e Save são discutidas em detalhes.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756540"
---
# <a name="ipapersave"></a><span data-ttu-id="ad0fb-104">IPaper:: salvar</span><span class="sxs-lookup"><span data-stu-id="ad0fb-104">IPaper::Save</span></span>

<span data-ttu-id="ad0fb-105">O foco principal neste código de exemplo é como o copapel pode carregar e salvar seus dados de papel em arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="ad0fb-106">As implementações do método [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)e **Save** são discutidas em detalhes.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="ad0fb-107">A seguir está o método **IPaper:: Save** do paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



<span data-ttu-id="ad0fb-108">Nesse relacionamento de cliente e servidor, o copaper não cria o arquivo composto usado para armazenar dados de papel.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="ad0fb-109">Para os métodos **Save** e [**Load**](ipaper--load.md) , o cliente passa um ponteiro de interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para um arquivo composto existente.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="ad0fb-110">Em seguida, ele usa o **IStorage** para gravar e ler dados nesse arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="ad0fb-111">Em **IPaper:: Save** acima, vários tipos de dados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="ad0fb-112">O CLSID para DllPaper, CLSID \_ DllPaper, é serializado e armazenado em um fluxo especial controlado pelo com dentro do objeto de armazenamento chamado " \\ 001CompObj".</span><span class="sxs-lookup"><span data-stu-id="ad0fb-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="ad0fb-113">A função de serviço [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) executa esse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="ad0fb-114">Esses dados CLSID armazenados podem ser usados para associar o conteúdo de armazenamento ao componente DllPaper que criou e pode interpretá-lo.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="ad0fb-115">Neste exemplo, o armazenamento raiz é passado por **StoClien** e, portanto, todo o arquivo composto é associado ao componente DllPaper.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="ad0fb-116">Esses dados CLSID podem ser recuperados posteriormente com uma chamada para a função de serviço [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .</span><span class="sxs-lookup"><span data-stu-id="ad0fb-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="ad0fb-117">Como o DllPaper lida com dados editáveis, também é apropriado registrar um formato de área de transferência no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="ad0fb-118">A função de serviço [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) é chamada para armazenar uma designação de formato de área de transferência e um nome legível pelo usuário para o formato.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="ad0fb-119">O nome legível pelo usuário destina-se à exibição de GUI nas listas de seleção.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="ad0fb-120">O nome passado acima usa uma macro, CLIPBDFMT \_ Str, que é definida como "DllPaper 1,0" em Paper. h.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="ad0fb-121">Esses dados armazenados da área de transferência podem ser recuperados posteriormente com uma chamada para a função de serviço [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span><span class="sxs-lookup"><span data-stu-id="ad0fb-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="ad0fb-122">Essa função retorna um valor de cadeia de caracteres que é alocado usando o alocador de memória de tarefa.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="ad0fb-123">O chamador é responsável por liberar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="ad0fb-124">**Salvar** avançar cria um fluxo no armazenamento para os dados de papel de copapel.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="ad0fb-125">O fluxo é chamado de "PAPERDATA" e é passado usando a \_ macro PAPERDATA USTR do Stream \_ .</span><span class="sxs-lookup"><span data-stu-id="ad0fb-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="ad0fb-126">O método [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requer que essa cadeia de caracteres esteja em Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="ad0fb-127">Como a cadeia de caracteres é fixa no tempo de compilação, a macro é definida como Unicode em Paper. h.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="ad0fb-128">O ' L' antes da cadeia de caracteres, indicando LONG, consegue isso.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="ad0fb-129">O método [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) cria e abre um fluxo dentro do armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="ad0fb-130">Um ponteiro de interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para o novo fluxo é passado em uma variável de ponteiro de interface do chamador.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="ad0fb-131">AddRef é chamado neste ponteiro de interface dentro de **CreateStream**, e o chamador deve liberar esse ponteiro depois de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="ad0fb-132">O método **CreateStream** é passado por vários sinalizadores de modo de acesso, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="ad0fb-133">STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_</span><span class="sxs-lookup"><span data-stu-id="ad0fb-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="ad0fb-134">[**STGM \_ CREATE**](stgm-constants.md) cria um novo fluxo ou substitui um existente de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="ad0fb-135">[**STGM \_ GRAVAR**](stgm-constants.md) abre o fluxo com permissão de gravação.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="ad0fb-136">[**STGM \_ DIRETO**](stgm-constants.md) abre o fluxo para acesso direto, em oposição ao acesso transacionado.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="ad0fb-137">[**STGM \_ COMPARTILHAMENTO \_ exclusivo**](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="ad0fb-138">Depois que o fluxo de PAPERDATA é criado com êxito, a interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) é usada para gravar no fluxo.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="ad0fb-139">O método **IStream:: Write** é usado para armazenar primeiro o conteúdo da estrutura de \_ Propriedades de papel.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="ad0fb-140">Esse é essencialmente um cabeçalho de propriedades na frente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="ad0fb-141">Como o número de versão é a primeira coisa no arquivo, ele pode ser lido de forma independente para determinar como lidar com os dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="ad0fb-142">Se a quantidade de dados realmente gravados não for igual à quantidade solicitada, o método Save será anulado e retornará STG \_ e \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="ad0fb-143">É simples salvar toda a matriz de dados de tinta no fluxo.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="ad0fb-144">Como o método [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opera em uma matriz de bytes, o número de bytes de dados de tinta armazenados na matriz é calculado e a operação de gravação começa no início da matriz.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="ad0fb-145">Se a quantidade de dados realmente gravados não for igual à quantidade solicitada, o método **Save** retornará STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="ad0fb-146">Depois que o fluxo é gravado, o método **IPaper:: Save** libera o ponteiro [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que ele estava usando.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="ad0fb-147">O método **Save** também chama o [**IPaperSink**](ipapersink-methods.md) do cliente (no método NotifySinks interno de copaper) para notificar o cliente de que a operação de salvamento foi concluída.</span><span class="sxs-lookup"><span data-stu-id="ad0fb-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="ad0fb-148">Neste ponto, o método **Save** retorna ao cliente de chamada, que normalmente liberará o ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="ad0fb-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




