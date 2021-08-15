---
title: IPaper salvar
description: O foco principal neste código de exemplo é como o copapel pode carregar e salvar seus dados de papel em arquivos compostos. As implementações do método IPaper, Load e Save são discutidas em detalhes.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52772002fe8f0ed234a4f430eaff4328f96f9d1ef151e83da3f4aa3e255dba09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961366"
---
# <a name="ipapersave"></a>IPaper:: salvar

O foco principal neste código de exemplo é como o copapel pode carregar e salvar seus dados de papel em arquivos compostos. As implementações do método [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)e **Save** são discutidas em detalhes.

A seguir está o método **IPaper:: Save** do paper. cpp.


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



Nesse relacionamento de cliente e servidor, o copaper não cria o arquivo composto usado para armazenar dados de papel. Para os métodos **Save** e [**Load**](ipaper--load.md) , o cliente passa um ponteiro de interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para um arquivo composto existente. Em seguida, ele usa o **IStorage** para gravar e ler dados nesse arquivo composto. Em **IPaper:: Save** acima, vários tipos de dados são armazenados.

O CLSID para DllPaper, CLSID \_ DllPaper, é serializado e armazenado em um fluxo especial controlado pelo com dentro do objeto de armazenamento chamado " \\ 001CompObj". A função de serviço [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) executa esse armazenamento. Esses dados CLSID armazenados podem ser usados para associar o conteúdo de armazenamento ao componente DllPaper que criou e pode interpretá-lo. Neste exemplo, o armazenamento raiz é passado por **StoClien** e, portanto, todo o arquivo composto é associado ao componente DllPaper. Esses dados CLSID podem ser recuperados posteriormente com uma chamada para a função de serviço [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .

Como o DllPaper lida com dados editáveis, também é apropriado registrar um formato de área de transferência no armazenamento. A função de serviço [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) é chamada para armazenar uma designação de formato de área de transferência e um nome legível pelo usuário para o formato. O nome legível pelo usuário destina-se à exibição de GUI nas listas de seleção. O nome passado acima usa uma macro, CLIPBDFMT \_ Str, que é definida como "DllPaper 1,0" em Paper. h. Esses dados armazenados da área de transferência podem ser recuperados posteriormente com uma chamada para a função de serviço [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Essa função retorna um valor de cadeia de caracteres que é alocado usando o alocador de memória de tarefa. O chamador é responsável por liberar a cadeia de caracteres.

**Salvar** avançar cria um fluxo no armazenamento para os dados de papel de copapel. O fluxo é chamado de "PAPERDATA" e é passado usando a \_ macro PAPERDATA USTR do Stream \_ . O método [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requer que essa cadeia de caracteres esteja em Unicode. Como a cadeia de caracteres é fixa no tempo de compilação, a macro é definida como Unicode em Paper. h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

O ' L' antes da cadeia de caracteres, indicando LONG, consegue isso.

O método [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) cria e abre um fluxo dentro do armazenamento especificado. Um ponteiro de interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para o novo fluxo é passado em uma variável de ponteiro de interface do chamador. AddRef é chamado neste ponteiro de interface dentro de **CreateStream**, e o chamador deve liberar esse ponteiro depois de usá-lo. O método **CreateStream** é passado por vários sinalizadores de modo de acesso, da seguinte maneira.

STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_

[**STGM \_ CREATE**](stgm-constants.md) cria um novo fluxo ou substitui um existente de mesmo nome. [**STGM \_ GRAVAR**](stgm-constants.md) abre o fluxo com permissão de gravação. [**STGM \_ DIRETO**](stgm-constants.md) abre o fluxo para acesso direto, em oposição ao acesso transacionado. [**STGM \_ COMPARTILHAMENTO \_ exclusivo**](stgm-constants.md) abre o arquivo para uso exclusivo e não compartilhado pelo chamador.

Depois que o fluxo de PAPERDATA é criado com êxito, a interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) é usada para gravar no fluxo. O método **IStream:: Write** é usado para armazenar primeiro o conteúdo da estrutura de \_ Propriedades de papel. Esse é essencialmente um cabeçalho de propriedades na frente do fluxo. Como o número de versão é a primeira coisa no arquivo, ele pode ser lido de forma independente para determinar como lidar com os dados a seguir. Se a quantidade de dados realmente gravados não for igual à quantidade solicitada, o método Save será anulado e retornará STG \_ e \_ CANTSAVE.

É simples salvar toda a matriz de dados de tinta no fluxo.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Como o método [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opera em uma matriz de bytes, o número de bytes de dados de tinta armazenados na matriz é calculado e a operação de gravação começa no início da matriz. Se a quantidade de dados realmente gravados não for igual à quantidade solicitada, o método **Save** retornará STG \_ E \_ CANTSAVE.

Depois que o fluxo é gravado, o método **IPaper:: Save** libera o ponteiro [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que ele estava usando.

O método **Save** também chama o [**IPaperSink**](ipapersink-methods.md) do cliente (no método NotifySinks interno de copaper) para notificar o cliente de que a operação de salvamento foi concluída. Neste ponto, o método **Save** retorna ao cliente de chamada, que normalmente liberará o ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

 

 




