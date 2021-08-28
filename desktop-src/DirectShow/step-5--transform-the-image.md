---
description: Use este exemplo para entender como o codificador RLE pode implementar o método como parte da escrita de um filtro de transformação.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: Etapa 5. Transformar a imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecbb2290b35347ccbc9b9821d423f7b3b26c9878187d09387dec914001df1a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650806"
---
# <a name="step-5-transform-the-image"></a>Etapa 5. Transformar a imagem

Esta é a etapa 5 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)

O filtro upstream fornece exemplos de mídia para o filtro de transformação chamando o método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada do filtro de transformação. Para processar os dados, o filtro de transformação chama **o método Transform,** que é virtual puro. As **classes CTransformFilter** **e CTransInPlaceFilter** usam duas versões diferentes desse método:

-   [**CTransformFilter::Transform**](ctransformfilter-transform.md) leva um ponteiro para o exemplo de entrada e um ponteiro para o exemplo de saída. Antes que o filtro chama o método , ele copia as propriedades de exemplo do exemplo de entrada para o exemplo de saída, incluindo os carimbos de data/hora.
-   [**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) leva um ponteiro para o exemplo de entrada. O filtro modifica os dados no local.

Se o **método Transform** retornar S \_ OK, o filtro entregará o downstream de exemplo. Para ignorar um quadro, retorne S \_ FALSE. Se houver um erro de streaming, retorne um código de falha.

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



Este exemplo presume que EncodeFrame é um método privado que implementa a codificação RLE. O próprio algoritmo de codificação não é descrito aqui; Para obter detalhes, consulte o tópico "Compactação de bitmap" na documentação do SDK da plataforma.

Primeiro, o exemplo chama [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) para recuperar os endereços dos buffers subjacentes. Ele os passa para o método encoderFrame privado. Em seguida, [**ele chama IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) para especificar o comprimento dos dados codificados. O filtro downstream precisa dessa informação para que possa gerenciar o buffer corretamente. Por fim, o método [**chama IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) para definir o sinalizador de quadro-chave como **TRUE.** A codificação de comprimento de run não usa quadros delta, portanto, cada quadro é um quadro-chave. Para quadros delta, de definido o valor como **FALSE.**

Outros problemas que você deve considerar incluem:

-   Carimbos de data/hora. A **classe CTransformFilter** timestamps o exemplo de saída antes de chamar o **método** Transform. Ele copia os valores de carimbo de data/hora do exemplo de entrada, sem modificá-los. Se o filtro precisar alterar os carimbos de data/hora, chame [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) no exemplo de saída.
-   Formatar alterações. O filtro upstream pode alterar formatos no meio do fluxo anexando um tipo de mídia ao exemplo. Antes de fazer isso, ele [**chama IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de entrada do filtro. Na classe **CTransformFilter,** isso resulta em uma chamada para **CheckInputType** seguida por **CheckTransform**. O filtro downstream também pode alterar os tipos de mídia usando o mesmo mecanismo. Em seu próprio filtro, há duas coisas a observar:

    -   Certifique-se **de que QueryAccept** não retorne falsas aceitaçãos.
    -   Se o filtro aceitar alterações de formato, verifique-as dentro do método **Transform** chamando [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). Se esse método retornar S \_ OK, o filtro deverá responder à alteração de formato.

    Para obter mais informações, consulte [Alterações de formato dinâmico.](dynamic-format-changes.md)

-   Tópicos. Em **CTransformFilter e** **CTransInPlaceFilter**, o filtro de transformação fornece amostras de saída de forma síncrona dentro do **método Receive.** O filtro não cria nenhum thread de trabalho para processar os dados. Normalmente, não há motivo para um filtro de transformação criar threads de trabalho.

Próximo: [Etapa 6. Adicione suporte para COM.](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



