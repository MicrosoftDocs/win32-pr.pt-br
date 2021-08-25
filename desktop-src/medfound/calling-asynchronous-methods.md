---
description: Chamando métodos assíncronos
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Chamando métodos assíncronos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959196"
---
# <a name="calling-asynchronous-methods"></a>Chamando métodos assíncronos

Em Media Foundation, muitas operações são executadas de forma assíncrona. As operações assíncronas podem melhorar o desempenho, pois não bloqueiam o thread de chamada. Uma operação assíncrona no Media Foundation é definida por um par de métodos com a Convenção de nomenclatura **begin...** e **end..**... Juntos, esses dois métodos definem uma operação de leitura assíncrona no fluxo.

Para iniciar uma operação assíncrona, chame o método **begin** . O método **begin** sempre contém pelo menos dois parâmetros:

-   Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . O aplicativo deve implementar essa interface.
-   Um ponteiro para um objeto de estado opcional.

A interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) notifica o aplicativo quando a operação é concluída. Para obter um exemplo de como implementar essa interface, consulte [implementando o retorno de chamada assíncrono](implementing-the-asynchronous-callback.md). O objeto de estado é opcional. Se especificado, ele deve implementar a interface **IUnknown** . Você pode usar o objeto de estado para armazenar qualquer informação de estado necessária para seu retorno de chamada. Se você não precisar de informações de estado, poderá definir esse parâmetro como **NULL**. O método **begin** pode conter parâmetros adicionais que são específicos para esse método.

Se o método **begin** retornar um código de falha, isso significará que a operação falhou imediatamente e o retorno de chamada não será invocado. Se o método **begin** for bem sucedido, isso significa que a operação está pendente e o retorno de chamada será invocado quando a operação for concluída.

Por exemplo, o método [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) inicia uma operação de leitura assíncrona em um fluxo de bytes:


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



O método de retorno de chamada é [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Ele tem um único parâmetro, *pAsyncResult*, que é um ponteiro para a interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Para concluir a operação assíncrona, chame o método **end** que corresponde ao método **begin** assíncrono. O método **end** sempre usa um ponteiro **IMFAsyncResult** . Sempre passe o mesmo ponteiro que você recebeu no método **Invoke** . A operação assíncrona não será concluída até que você chame o método **end** . Você pode chamar o método **end** de dentro do método **Invoke** ou pode chamá-lo de outro thread.

Por exemplo, para concluir o [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) em um fluxo de bytes, chame [**IMFByteStream:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



O valor de retorno do método **end** indica o status da operação assíncrona. Na maioria dos casos, seu aplicativo executará algum trabalho depois que a operação assíncrona for concluída, independentemente de ser concluída com êxito ou não. Você tem várias opções:

-   Faça o trabalho dentro do método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Essa abordagem é aceitável, desde que seu aplicativo nunca bloqueie o thread de chamada ou espere qualquer coisa dentro do método **Invoke** . Se você bloquear o thread de chamada, poderá bloquear o pipeline de streaming. Por exemplo, você pode atualizar algumas variáveis de estado, mas não executar uma operação de leitura síncrona ou esperar um objeto mutex.
-   No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , defina um evento e retorne imediatamente. O thread de chamada do aplicativo aguarda o evento e faz o trabalho quando o evento é sinalizado.
-   No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , poste uma mensagem de janela privada na janela do aplicativo e retorne imediatamente. O aplicativo faz o trabalho em seu loop de mensagem. (Certifique-se de postar a mensagem chamando **a mensagem post, não** **SendMessage**, porque **SendMessage** pode bloquear o thread de retorno de chamada.)

É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de outro thread. Seu aplicativo é responsável por garantir que qualquer trabalho realizado dentro de **Invoke** seja thread-safe.

Por padrão, o thread que chama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) não faz nenhuma suposição sobre o comportamento do seu objeto de retorno de chamada. Opcionalmente, você pode implementar o método [**IMFAsyncCallback:: Parameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) para retornar informações sobre sua implementação de retorno de chamada. Caso contrário, esse método pode retornar **E \_ NOTIMPL**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Se você especificou um objeto de estado no método **begin** , poderá recuperá-lo de dentro do seu método de retorno de chamada chamando [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md)
</dt> </dl>

 

 



