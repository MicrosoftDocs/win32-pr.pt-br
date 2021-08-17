---
title: Recebendo mensagens de erro de um sink
description: Recebendo mensagens de erro de um sink
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- ASF (Advanced Systems Format), mensagens de erro de sinks
- ASF (Formato de Sistemas Avançados), mensagens de erro de sinks
- ASF (Advanced Systems Format), sinks
- ASF (Formato de Sistemas Avançados), sinks
- sinks, mensagens de erro
- mensagens de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e432f805b5e33de0e830a2f319713bccec328d429f8eb04064d87edc56bf375c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930866"
---
# <a name="getting-error-messages-from-a-sink"></a>Recebendo mensagens de erro de um sink

O objeto writer não envia mensagens para o método de retorno de chamada [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) No entanto, você pode definir os sinks de writer para enviar mensagens para OnStatus. Cada sink deve ser definido para entregar o status separadamente, mas todos os sinks podem relatar para o mesmo retorno de chamada.

Para definir um sink para entregar mensagens de status para **OnStatus,** chame o [**método IWMRegisterCallback::Advise.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise)

O código de exemplo a seguir demonstra como definir todos os sinks para entregar mensagens de status para um retorno de chamada **OnStatus.** Neste exemplo, o índice de cada sink será usado como o parâmetro de contexto para que o **método OnStatus** possa diferenciar entre mensagens dos diferentes sinks. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMRegisterCallback Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




