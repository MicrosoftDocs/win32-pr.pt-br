---
description: Dando suporte a vários retornos de chamada
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Dando suporte a vários retornos de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661822"
---
# <a name="supporting-multiple-callbacks"></a>Dando suporte a vários retornos de chamada

Se você chamar mais de um método assíncrono, cada um deles exigirá uma implementação separada de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). No entanto, talvez você queira implementar os retornos de chamada dentro de uma única classe C++. A classe pode ter apenas um método **Invoke** , portanto, uma solução é fornecer uma classe auxiliar **que delega chamadas** a outro método em uma classe de contêiner.

O código a seguir mostra um modelo de classe chamado `AsyncCallback` , que demonstra essa abordagem.


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



O parâmetro de modelo é o nome da classe de contêiner. O `AsyncCallback` Construtor tem dois parâmetros: um ponteiro para a classe de contêiner e o endereço de um método de retorno de chamada na classe de contêiner. A classe de contêiner pode ter várias instâncias da `AsyncCallback` classe como variáveis de membro, uma para cada método assíncrono. Quando a classe de contêiner chama um método assíncrono, ela usa a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do `AsyncCallback` objeto apropriado. Quando o `AsyncCallback` método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto é chamado, a chamada é delegada para o método correto na classe de contêiner.

O `AsyncCallback` objeto também Delega chamadas **AddRef** e **Release** para a classe de contêiner, de modo que a classe de contêiner gerencia o tempo de vida do `AsyncCallback` objeto. Isso garante que o `AsyncCallback` objeto não será excluído até que o próprio objeto de contêiner seja excluído.

O código a seguir mostra como usar este modelo:


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



Neste exemplo, a classe de contêiner é nomeada `CMyObject` . A variável de membro de *\_ CB m* é um `AsyncCallback` objeto. No `CMyObject` Construtor, a variável de membro de *\_ CB m* é inicializada com o endereço do `CMyObject::OnInvoke` método.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md)
</dt> </dl>

 

 



