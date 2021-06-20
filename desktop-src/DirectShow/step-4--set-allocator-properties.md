---
description: Definir propriedades do alocador como parte da escrita de um filtro de transformação. O pino de saída do filtro de transformação seleciona o alocador downstream.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Etapa 4. Definir propriedades do alocador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406819"
---
# <a name="step-4-set-allocator-properties"></a>Etapa 4. Definir propriedades do alocador

Esta é a etapa 4 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)

> [!Note]  
> Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter.**

 

Depois que dois pinos concordarem com um tipo de mídia, eles selecionarão um alocador para a conexão e negociarão as propriedades do alocador, como o tamanho do buffer e o número de buffers.

Na classe **CTransformFilter,** há dois alocadores, um para a conexão de pino upstream e outro para a conexão de pino downstream. O filtro upstream seleciona o alocador upstream e também escolhe as propriedades do alocador. O pino de entrada aceita qualquer decisão do filtro upstream. Se você precisar modificar esse comportamento, substitua o [**método CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)

O pino de saída do filtro de transformação seleciona o alocador downstream. Ele executa as seguintes etapas:

1.  Se o filtro downstream puder fornecer um alocador, o pino de saída usará esse. Caso contrário, o pino de saída criará um novo alocador.
2.  O pino de saída obtém os requisitos de alocador do filtro downstream (se algum) chamando [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  O pino de saída chama o método [**CTransformFilter::D eformBufferSize**](ctransformfilter-decidebuffersize.md) do filtro de transformação, que é virtual puro. Os parâmetros para esse método são um ponteiro para o alocador e uma estrutura [**ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) com os requisitos do filtro downstream. Se o filtro downstream não tiver requisitos de alocador, a estrutura será zerada.
4.  No método **DecideBufferSize,** a classe derivada define as propriedades do alocador chamando [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

Em geral, a classe derivada selecionará as propriedades do alocador com base no formato de saída, nos requisitos do filtro downstream e nos próprios requisitos do filtro. Tente selecionar propriedades compatíveis com a solicitação do filtro downstream. Caso contrário, o filtro downstream poderá rejeitar a conexão.

No exemplo a seguir, o codificador RLE define valores mínimos para o tamanho do buffer, o alinhamento do buffer e a contagem de buffers. Para o prefixo, ele usa qualquer valor que o filtro downstream solicitou. O prefixo normalmente é zero bytes, mas alguns filtros o exigem. Por exemplo, o [filtro AVI Mux](avi-mux-filter.md) usa o prefixo para gravar os títulos DEIS.


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



O alocador pode não ser capaz de corresponder exatamente à sua solicitação. Portanto, o **método SetProperties** retorna o resultado real em uma estrutura **ALLOCATOR \_ PROPERTIES** separada (o parâmetro *Real,* no exemplo anterior). Mesmo quando **SetProperties for** bem-sucedido, você deverá verificar o resultado para garantir que eles atendem aos requisitos mínimos do filtro.

**Alocadores personalizados**

Por padrão, todas as classes de filtro usam a [**classe CMemAllocator**](cmemallocator.md) para seus alocadores. Essa classe aloca memória do espaço de endereço virtual do processo do cliente (usando **VirtualAlloc**). Se o filtro precisar usar algum outro tipo de memória, como superfícies directDraw, você poderá implementar um alocador personalizado. Você pode usar a [**classe CBaseAllocator**](cbaseallocator.md) ou escrever uma classe de alocador totalmente nova. Se o filtro tiver um alocador personalizado, substitua os seguintes métodos, dependendo de qual pino usa o alocador:

-   Pino de entrada: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin::NotifyAllocator.**](cbaseinputpin-notifyallocator.md)
-   Pino de saída: [**CBaseOutputPin::D eputaçãoAllocator**](cbaseoutputpin-decideallocator.md).

Se o outro filtro se recusar a se conectar usando seu alocador personalizado, o filtro poderá falhar na conexão ou conectar-se ao alocador do outro filtro. No último caso, talvez seja necessário definir um sinalizador interno indicando o tipo de alocador. Para ver um exemplo dessa abordagem, consulte [**Classe CDrawImage**](cdrawimage.md).

Próximo: [Etapa 5. Transforme a Imagem](step-5--transform-the-image.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



