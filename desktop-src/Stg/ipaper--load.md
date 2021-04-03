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
# <a name="ipaperload"></a>IPaper:: Load

O código de exemplo C++ a seguir mostra como abrir o fluxo existente no armazenamento, ler novas propriedades de papel no e defini-las como os valores atuais para o copapel.

Este é o método **IPaper:: Load** do paper. cpp.


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



Agora, o método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) é chamado para abrir o fluxo existente no armazenamento chamado "PAPERDATA". Os sinalizadores de modo de acesso são para acesso exclusivo de somente leitura, direto e não compartilhado. Quando o fluxo é aberto, o método [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) é chamado para ler a estrutura de propriedades do papel \_ . Se a quantidade realmente lida não for igual à quantidade solicitada, a operação de carregamento será anulada e e a \_ falha será retornada. Se a versão de formato nas propriedades de papel recém-lidas \_ não for reconhecida, a operação de carregamento será anulada e a **carga** retornará e \_ falhará.

Com uma versão de formato de dados de tinta válida, o tamanho da nova matriz de dados de tinta das propriedades de papel \_ que foi lida no é usado para alocar uma nova matriz de dados de tinta do tamanho necessário. Os dados de tinta existentes são excluídos e seus dados são perdidos. Se esses dados eram valiosos, eles devem ter sido salvos antes de o **carregamento** ser chamado. Depois que a nova matriz é alocada, [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) é chamado novamente para ler os dados na matriz a partir do fluxo. Se essa chamada for bem sucedido, os valores nas propriedades de papel recém lidas serão adotados como os valores atuais para o copaper.

Durante essa operação de carregamento, uma estrutura de propriedades de papel temporária \_ , NewProps, foi usada para manter as novas propriedades lidas. Se tudo tiver sucesso com a carga, NewProps será copiado para a \_ estrutura de propriedades do papel, m \_ paperproperties. Como antes, depois que a carga é feita e o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) não é mais necessário, o ponteiro **IStream** é liberado.

Se houver um erro no final da **carga**, a matriz de dados de tinta será apagada, pois pode conter dados danificados.

Se não houver nenhum erro no final da **carga**, o método [**IPaperSink:: Loaded**](ipapersink-methods.md) do cliente será chamado, no método NotifySinks interno de copapel, para notificar o cliente de que a operação de carregamento foi concluída. Essa é uma notificação importante para o cliente, pois ele deve exibir esses novos dados de tinta carregados. Essa notificação faz uso significativo de recursos de objetos conectáveis no copaper.

 

 




