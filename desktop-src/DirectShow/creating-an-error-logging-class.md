---
description: Este tópico descreve como implementar o log de erros nos serviços de edição do DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Criando uma classe de log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105752081"
---
# <a name="creating-an-error-logging-class"></a>Criando uma classe de log de erros

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este tópico descreve como implementar o log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md).

Primeiro, declare uma classe que irá implementar o log de erros. A classe herda a interface [**IAMErrorLog**](iamerrorlog.md) . Ele contém declarações para os três métodos **IUnknown** e para o método único em [IAMErrorLog](implementing-iamerrorlog.md). A declaração de classe é a seguinte:


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



A única variável de membro na classe é m \_ lRef, que contém a contagem de referência do objeto.

Em seguida, defina os métodos em **IUnknown**. O exemplo a seguir mostra uma implementação padrão para esses métodos:


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



Com a estrutura COM em vigor, agora você pode implementar a interface **IAMErrorLog** . A próxima seção descreve como fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de log](logging-errors.md)
</dt> </dl>

 

 



