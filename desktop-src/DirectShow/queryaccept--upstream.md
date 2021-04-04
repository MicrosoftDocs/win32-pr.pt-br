---
description: QueryAccept (upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: QueryAccept (upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646048"
---
# <a name="queryaccept-upstream"></a>QueryAccept (upstream)

Esse mecanismo permite que um PIN de entrada proponha uma alteração de formato ao seu ponto de upstream. O filtro downstream deve anexar um tipo de mídia ao exemplo que o filtro upstream obterá em sua próxima chamada para [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer). No entanto, para fazer isso, o filtro downstream deve fornecer um alocador personalizado para a conexão. Esse alocador deve implementar um método privado que o filtro downstream possa usar para definir o tipo de mídia no próximo exemplo.

Ocorrem as seguintes etapas:

1.  O filtro downstream verifica se a conexão do PIN usa o alocador personalizado do filtro. Se o filtro upstream possuir o alocador, o filtro downstream não poderá alterar o formato.
2.  O filtro downstream chama [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída upstream (veja A ilustração, etapa A).
3.  Se `QueryAccept` o retornar S \_ OK, o filtro downstream chamará o método particular em seu alocador para definir o tipo de mídia. Dentro desse método particular, o alocador chama [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) no próximo exemplo disponível (B).
4.  O filtro upstream chama **GetBuffer** para obter um novo exemplo (C) e [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) para obter o tipo de mídia (D).
5.  Quando o filtro upstream entrega o exemplo, ele deve deixar o tipo de mídia anexado a esse exemplo. Dessa forma, o filtro downstream pode confirmar que o tipo de mídia foi alterado (E).

Se o filtro upstream aceitar a alteração de formato, ele também deverá ser capaz de voltar para o tipo de mídia original, conforme mostrado no diagrama a seguir.

![QueryAccept (upstream)](images/dynformat4.png)

Os principais exemplos desse tipo de alteração de formato envolvem os processadores de vídeo do DirectShow.

-   O filtro de [processamento de vídeo](video-renderer-filter.md) original pode alternar entre os tipos RGB e YUV durante o streaming. Quando o filtro se conecta, ele requer um formato RGB que corresponda às configurações de exibição atuais. Isso garante que ele possa fazer fallback no GDI se precisar. Após o streaming começar, se o DirectDraw estiver disponível, o processador de vídeo solicitará uma alteração de formato para um tipo YUV. Posteriormente, ele poderá voltar para RGB se perder a superfície do DirectDraw por qualquer motivo.
-   O filtro de processador de mixagem de vídeo (VMR) mais recente se conectará a qualquer formato com suporte pelo hardware de gráficos, incluindo tipos YUV. No entanto, o hardware de gráficos pode alterar o stride da superfície do DirectDraw subjacente para otimizar o desempenho. O filtro VMR usa `QueryAccept` para relatar o novo Stride, que é especificado no membro de **bilargura** da estrutura **BITMAPINFOHEADER** . Os retângulos de origem e de destino na estrutura **VIDEOINFOHEADER** ou **VIDEOINFOHEADER2** identificam a região onde o vídeo deve ser decodificado.

**Observação de implementação**

É improvável que você escreva um filtro que precisa solicitar alterações no formato upstream, pois isso é principalmente um recurso de renderizadores de vídeo. No entanto, se você escrever um filtro de transformação de vídeo ou um decodificador de vídeo, o filtro deverá responder corretamente a solicitações do processador de vídeo.

Um filtro de trans-in-Place que fica entre o processador de vídeo e o decodificador deve passar todas as `QueryAccept` chamadas upstream. Armazene as novas informações de formato quando ele chegar.

Um filtro de cópia/transformação (ou seja, um filtro não trans-in-Place) deve implementar um dos seguintes comportamentos:

-   O formato aprovado muda de fluxo e armazena as novas informações de formato quando ele chega. O filtro deve usar um alocador personalizado para que ele possa anexar o formato ao exemplo de upstream.
-   Execute a conversão de formato dentro do filtro. Isso é provavelmente mais fácil do que passar a alteração de formato upstream. No entanto, pode ser menos eficiente do que permitir que o filtro do decodificador decodifique o formato correto.
-   Como último recurso, basta rejeitar a alteração do formato. (Para obter mais informações, consulte o código-fonte para o método [**CTransInPlaceOutputPin:: CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) na biblioteca de classes base do DirectShow.) A rejeição de uma alteração de formato pode reduzir o desempenho, no entanto, porque impede que o renderizador de vídeo Use o formato mais eficiente.

O pseudocódigo a seguir mostra como você pode implementar um filtro de cópia/transformação (derivado de **CTransformFilter**) que pode alternar entre os tipos de saída YUV e RGB. Este exemplo pressupõe que o filtro faz a conversão em si, em vez de passar a alteração de formato upstream.


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



