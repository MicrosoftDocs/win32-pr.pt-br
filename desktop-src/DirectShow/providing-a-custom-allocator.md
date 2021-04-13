---
description: Fornecendo um alocador personalizado
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Fornecendo um alocador personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370151"
---
# <a name="providing-a-custom-allocator"></a>Fornecendo um alocador personalizado

Esta seção descreve como fornecer um alocador personalizado para um filtro. Somente as conexões [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) são descritas, mas as etapas para uma conexão [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) são semelhantes.

Primeiro, defina uma classe C++ para o alocador. Seu alocador pode derivar de uma das classes de alocador padrão, [**CBaseAllocator**](cbaseallocator.md) ou [**CMemAllocator**](cmemallocator.md), ou você pode criar uma classe de alocador totalmente nova. Se você criar uma nova classe, ela deverá expor a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

As etapas restantes dependem se o alocador pertence a um PIN de entrada ou a um pino de saída no filtro. Os Pins de entrada desempenham uma função diferente dos Pins de saída durante a fase de negociação de alocador, pois o PIN de saída seleciona o alocador.

**Fornecendo um alocador personalizado para um PIN de entrada**

Para fornecer um alocador para um PIN de entrada, substitua o método [**CBaseInputPin:: Getalocador**](cbaseinputpin-getallocator.md) de entrada do PIN. Dentro desse método, verifique a variável de membro **m \_ pAllocator** . Se essa variável for não **nula**, significa que o alocador já foi selecionado para essa conexão, portanto, o método **getalocador** deve retornar um ponteiro para esse alocador. Se **m \_ PAllocator** for **nulo**, isso significará que o alocador não foi selecionado, portanto, o método **getalocador** deve retornar um ponteiro para o alocador preferencial do pino de entrada. Nesse caso, crie uma instância do seu alocador personalizado e retorne seu ponteiro [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . O código a seguir mostra como implementar o método **Getalocador** :


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Quando o filtro upstream seleciona um alocador, ele chama o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) do pino de entrada. Substitua o método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) para verificar as propriedades do alocador. Em alguns casos, o PIN de entrada poderá rejeitar o alocador se ele não for seu alocador personalizado, embora isso possa causar uma falha na conexão inteira do PIN.

**Fornecendo um alocador personalizado para um pino de saída**

Para fornecer um alocador para um pino de saída, substitua o método [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) para criar uma instância do seu alocador:


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Por padrão, a classe [**CBaseOutputPin**](cbaseoutputpin.md) solicita um alocador do PIN de entrada primeiro. Se esse alocador não for adequado, o pino de saída criará seu próprio alocador. Para forçar a conexão a usar seu alocador personalizado, substitua o método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) . No entanto, lembre-se de que isso pode impedir que o PIN de saída se conecte a determinados filtros, porque o outro filtro também pode exigir seu próprio alocador personalizado. Uma terceira opção é alternar a ordem: Tente o seu alocador personalizado primeiro e, em seguida, volte para o alocador do outro filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Negociando alocadores](negotiating-allocators.md)
</dt> </dl>

 

 



