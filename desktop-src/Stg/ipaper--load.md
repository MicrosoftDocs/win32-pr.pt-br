---
title: IPaper carga
description: O código de exemplo C++ a seguir mostra como abrir o fluxo existente no armazenamento, ler novas propriedades de papel no e defini-las como os valores atuais para o copapel.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- IPaper carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916508"
---
# <a name="ipaperload"></a><span data-ttu-id="a1a54-104">IPaper:: Load</span><span class="sxs-lookup"><span data-stu-id="a1a54-104">IPaper::Load</span></span>

<span data-ttu-id="a1a54-105">O código de exemplo C++ a seguir mostra como abrir o fluxo existente no armazenamento, ler novas propriedades de papel no e defini-las como os valores atuais para o copapel.</span><span class="sxs-lookup"><span data-stu-id="a1a54-105">The following C++ sample code shows how to open the existing stream in the storage, read new paper properties in and then set them as the current values for COPaper.</span></span>

<span data-ttu-id="a1a54-106">Este é o método **IPaper:: Load** do paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="a1a54-106">The following is the **IPaper::Load** method from Paper.cpp.</span></span>


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



<span data-ttu-id="a1a54-107">Agora, o método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) é chamado para abrir o fluxo existente no armazenamento chamado "PAPERDATA".</span><span class="sxs-lookup"><span data-stu-id="a1a54-107">Now, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method is called to open the existing stream in the storage called "PAPERDATA".</span></span> <span data-ttu-id="a1a54-108">Os sinalizadores de modo de acesso são para acesso exclusivo de somente leitura, direto e não compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a1a54-108">Access mode flags are for read-only, direct, and non-shared exclusive access.</span></span> <span data-ttu-id="a1a54-109">Quando o fluxo é aberto, o método [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) é chamado para ler a estrutura de propriedades do papel \_ .</span><span class="sxs-lookup"><span data-stu-id="a1a54-109">When the stream is open, the [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) method is called to read the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="a1a54-110">Se a quantidade realmente lida não for igual à quantidade solicitada, a operação de carregamento será anulada e e a \_ falha será retornada.</span><span class="sxs-lookup"><span data-stu-id="a1a54-110">If the amount actually read does not equal the amount requested, the load operation is aborted, and E\_FAIL is returned.</span></span> <span data-ttu-id="a1a54-111">Se a versão de formato nas propriedades de papel recém-lidas \_ não for reconhecida, a operação de carregamento será anulada e a **carga** retornará e \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="a1a54-111">If the format version in the newly read PAPER\_PROPERTIES is not recognized, then the load operation is aborted and **Load** returns E\_FAIL.</span></span>

<span data-ttu-id="a1a54-112">Com uma versão de formato de dados de tinta válida, o tamanho da nova matriz de dados de tinta das propriedades de papel \_ que foi lida no é usado para alocar uma nova matriz de dados de tinta do tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="a1a54-112">With a valid ink data format version, the size of the new ink data array from the PAPER\_PROPERTIES that was read in is used to allocate a new ink data array of the required size.</span></span> <span data-ttu-id="a1a54-113">Os dados de tinta existentes são excluídos e seus dados são perdidos.</span><span class="sxs-lookup"><span data-stu-id="a1a54-113">The existing ink data is deleted, and its data is lost.</span></span> <span data-ttu-id="a1a54-114">Se esses dados eram valiosos, eles devem ter sido salvos antes de o **carregamento** ser chamado.</span><span class="sxs-lookup"><span data-stu-id="a1a54-114">If this data was valuable, it should have been saved before **Load** was called.</span></span> <span data-ttu-id="a1a54-115">Depois que a nova matriz é alocada, [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) é chamado novamente para ler os dados na matriz a partir do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a1a54-115">After the new array is allocated, [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) is called again to read the data into the array from the stream.</span></span> <span data-ttu-id="a1a54-116">Se essa chamada for bem sucedido, os valores nas propriedades de papel recém lidas serão adotados como os valores atuais para o copaper.</span><span class="sxs-lookup"><span data-stu-id="a1a54-116">If this call succeeds, the values in the newly read paper properties are adopted as the current values for COPaper.</span></span>

<span data-ttu-id="a1a54-117">Durante essa operação de carregamento, uma estrutura de propriedades de papel temporária \_ , NewProps, foi usada para manter as novas propriedades lidas.</span><span class="sxs-lookup"><span data-stu-id="a1a54-117">During this load operation, a temporary PAPER\_PROPERTIES structure, NewProps, was used to hold the new properties read in.</span></span> <span data-ttu-id="a1a54-118">Se tudo tiver sucesso com a carga, NewProps será copiado para a \_ estrutura de propriedades do papel, m \_ paperproperties.</span><span class="sxs-lookup"><span data-stu-id="a1a54-118">If all succeeds with the load, NewProps is copied into the PAPER\_PROPERTIES structure, m\_PaperProperties.</span></span> <span data-ttu-id="a1a54-119">Como antes, depois que a carga é feita e o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) não é mais necessário, o ponteiro **IStream** é liberado.</span><span class="sxs-lookup"><span data-stu-id="a1a54-119">As before, after Load is done and the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is no longer required, the **IStream** pointer is released.</span></span>

<span data-ttu-id="a1a54-120">Se houver um erro no final da **carga**, a matriz de dados de tinta será apagada, pois pode conter dados danificados.</span><span class="sxs-lookup"><span data-stu-id="a1a54-120">If there is an error at the end of **Load**, the ink data array is erased, because it may contain damaged data.</span></span>

<span data-ttu-id="a1a54-121">Se não houver nenhum erro no final da **carga**, o método [**IPaperSink:: Loaded**](ipapersink-methods.md) do cliente será chamado, no método NotifySinks interno de copapel, para notificar o cliente de que a operação de carregamento foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a1a54-121">If there is no error at the end of **Load**, the client [**IPaperSink::Loaded**](ipapersink-methods.md) method is called, in the COPaper internal NotifySinks method, to notify the client that the load operation is completed.</span></span> <span data-ttu-id="a1a54-122">Essa é uma notificação importante para o cliente, pois ele deve exibir esses novos dados de tinta carregados.</span><span class="sxs-lookup"><span data-stu-id="a1a54-122">This is an important notification for the client, because it must display this new loaded ink data.</span></span> <span data-ttu-id="a1a54-123">Essa notificação faz uso significativo de recursos de objetos conectáveis no copaper.</span><span class="sxs-lookup"><span data-stu-id="a1a54-123">This notification makes significant use of connectable object features in COPaper.</span></span>

 

 




