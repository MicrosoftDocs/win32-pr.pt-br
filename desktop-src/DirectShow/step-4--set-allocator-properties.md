---
description: Etapa 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Etapa 4. Definir propriedades de alocador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787132"
---
# <a name="step-4-set-allocator-properties"></a>Etapa 4. Definir propriedades de alocador

Esta é a etapa 4 do tutorial [escrevendo filtros de transformação](writing-transform-filters.md).

> [!Note]  
> Esta etapa não é necessária para filtros que derivam de **CTransInPlaceFilter**.

 

Depois que dois Pins concordam em um tipo de mídia, eles selecionam um alocador para a conexão e negociam as propriedades do alocador, como o tamanho do buffer e o número de buffers.

Na classe **CTransformFilter** , há dois alocadores, um para a conexão de PIN upstream e outro para a conexão de PIN de downstream. O filtro upstream seleciona o alocador upstream e também escolhe as propriedades do alocador. O PIN de entrada aceita tudo o que o filtro upstream decide. Se você precisar modificar esse comportamento, substitua o método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) .

O pino de saída do filtro de transformação seleciona o alocador downstream. Ele executa as seguintes etapas:

1.  Se o filtro downstream puder fornecer um alocador, o PIN de saída usará aquele. Caso contrário, o pino de saída criará um novo alocador.
2.  O pino de saída Obtém os requisitos de alocador do filtro downstream (se houver) chamando [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).
3.  O pino de saída chama o método [**CTransformFilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) do filtro de transformação, que é virtual puro. Os parâmetros para esse método são um ponteiro para o alocador e uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) com os requisitos do filtro downstream. Se o filtro downstream não tiver requisitos de alocador, a estrutura será zerada.
4.  No método **DecideBufferSize** , a classe derivada define as propriedades do alocador chamando [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).

Em geral, a classe derivada selecionará as propriedades do alocador com base no formato de saída, os requisitos do filtro downstream e os requisitos próprios do filtro. Tente selecionar as propriedades que são compatíveis com a solicitação do filtro downstream. Caso contrário, o filtro downstream poderá rejeitar a conexão.

No exemplo a seguir, o codificador RLE define valores mínimos para o tamanho do buffer, o alinhamento do buffer e a contagem de buffers. Para o prefixo, ele usa qualquer valor que o filtro downstream solicitou. O prefixo geralmente é zero bytes, mas alguns filtros exigem isso. Por exemplo, o filtro [AVI Mux](avi-mux-filter.md) usa o prefixo para gravar cabeçalhos riff.


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



O alocador pode não ser capaz de corresponder exatamente à sua solicitação. Portanto, o método **SetProperties** retorna o resultado real em uma estrutura **de \_ Propriedades de alocador** separada (o parâmetro *real* , no exemplo anterior). Mesmo quando **SetProperties** é executado com sucesso, você deve verificar o resultado para garantir que eles atendam aos requisitos mínimos do seu filtro.

**Alocadores personalizados**

Por padrão, todas as classes de filtro usam a classe [**CMemAllocator**](cmemallocator.md) para seus alocadores. Essa classe aloca memória do espaço de endereço virtual do processo do cliente (usando o **VirtualAlloc**). Se o filtro precisar usar algum outro tipo de memória, como as superfícies do DirectDraw, você poderá implementar um alocador personalizado. Você pode usar a classe [**CBaseAllocator**](cbaseallocator.md) ou escrever uma classe de alocador totalmente nova. Se o filtro tiver um alocador personalizado, substitua os seguintes métodos, dependendo de qual PIN usa o alocador:

-   Pino de entrada: [**CBaseInputPin:: Getalocator**](cbaseinputpin-getallocator.md) e [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md).
-   Pino de saída: [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

Se o outro filtro se recusar a se conectar usando seu alocador personalizado, o filtro poderá falhar na conexão ou conectar-se com o alocador do outro filtro. No último caso, talvez seja necessário definir um sinalizador interno que indique o tipo de alocador. Para obter um exemplo dessa abordagem, consulte [**classe CDrawImage**](cdrawimage.md).

Em seguida: [etapa 5. Transforme a imagem](step-5--transform-the-image.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



