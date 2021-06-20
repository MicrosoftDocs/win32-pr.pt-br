---
description: Use este exemplo para entender como o codificador RLE pode implementar o método como parte da gravação de um filtro de transformação.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Etapa 5. Transformar a imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406779"
---
# <a name="step-5-transform-the-image"></a>Etapa 5. Transformar a imagem

Esta é a etapa 5 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

O filtro upstream fornece amostras de mídia para o filtro de transformação chamando o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada do filtro de transformação. Para processar os dados, o filtro de transformação chama o método **Transform** , que é virtual puro. As classes **CTransformFilter** e **CTransInPlaceFilter** usam duas versões diferentes desse método:

-   [**CTransformFilter:: Transform**](ctransformfilter-transform.md) usa um ponteiro para o exemplo de entrada e um ponteiro para o exemplo de saída. Antes que o filtro chame o método, ele copia as propriedades de exemplo do exemplo de entrada para o exemplo de saída, incluindo os carimbos de data/hora.
-   [**CTransInPlaceFilter:: Transform**](ctransinplacefilter-transform.md) usa um ponteiro para o exemplo de entrada. O filtro modifica os dados no local.

Se o método **Transform** retornar S \_ OK, o filtro entregará o exemplo downstream. Para ignorar um quadro, retorne S \_ false. Se houver um erro de streaming, retorne um código de falha.

O exemplo a seguir mostra como o codificador RLE pode implementar esse método. Sua própria implementação pode diferir consideravelmente, dependendo do que o filtro faz.


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



Este exemplo pressupõe que EncodeFrame é um método particular que implementa a codificação RLE. O próprio algoritmo de codificação não é descrito aqui; para obter detalhes, consulte o tópico "compactação de bitmap" na documentação do Platform SDK.

Primeiro, o exemplo chama [**IMediaSample:: Getapontarr**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar os endereços dos buffers subjacentes. Ele passa esses para o método EncoderFrame privado. Em seguida, ele chama [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) para especificar o comprimento dos dados codificados. O filtro downstream precisa dessas informações para que possa gerenciar o buffer corretamente. Por fim, o método chama [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) para definir o sinalizador de quadro de chave como **true**. A codificação de comprimento de execução não usa quadros Delta, portanto, cada quadro é um quadro-chave. Para quadros Delta, defina o valor como **false**.

Outros problemas que você deve considerar incluem:

-   Carimbos de data/hora. A classe **CTransformFilter** carimbo de data/hora o exemplo de saída antes de chamar o método **Transform** . Ele copia os valores de carimbo de data/hora do exemplo de entrada, sem modificá-los. Se o filtro precisar alterar os carimbos de data/hora, chame [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) no exemplo de saída.
-   Formatar alterações. O filtro upstream pode alterar formatos MID-Stream anexando um tipo de mídia ao exemplo. Antes de fazer isso, ele chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no PIN de entrada do seu filtro. Na classe **CTransformFilter** , isso resulta em uma chamada para **CheckInputType** seguida por **CheckTransform**. O filtro downstream também pode alterar os tipos de mídia, usando o mesmo mecanismo. Em seu próprio filtro, há duas coisas a serem observadas:

    -   Certifique-se de que **QueryAccept** não retorna falsos aceitações.
    -   Se o filtro aceitar alterações de formato, verifique-as dentro do método **Transform** chamando [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se esse método retornar S \_ OK, o filtro deverá responder à alteração de formato.

    Para obter mais informações, consulte [Dynamic Format Changes](dynamic-format-changes.md).

-   Threads. Em **CTransformFilter** e **CTransInPlaceFilter**, o filtro de transformação fornece amostras de saída de forma síncrona dentro do método **Receive** . O filtro não cria nenhum thread de trabalho para processar os dados. Normalmente, não há motivo para um filtro de transformação criar threads de trabalho.

Em seguida: [etapa 6. Adicione suporte para COM](step-6--add-support-for-com.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



