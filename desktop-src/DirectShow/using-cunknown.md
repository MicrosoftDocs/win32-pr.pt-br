---
description: DirectShow implementa IUnknown em uma classe base chamada CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Usando CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211ebf8c581502665c5f07b3720759efc7afab75a05a49a68f9945029dd6cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051376"
---
# <a name="using-cunknown"></a>Usando CUnknown

DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) em uma classe base chamada [**CUnknown**](cunknown.md). Você pode usar **CUnknown** para derivar outras classes, substituindo somente os métodos que mudam entre os componentes. a maioria das outras classes base em DirectShow deriva de **CUnknown**, de modo que seu componente pode herdar diretamente do **CUnknown** ou de outra classe base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md). Ele gerencia contagens de referência internamente e, na maioria das situações, sua classe derivada pode herdar os dois métodos de contagem de referência sem alteração. Lembre-se de que o **CUnknown** se exclui quando a contagem de referência cai para zero. Por outro lado, você deve substituir [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), porque o método na classe base retorna E \_ nointerface se receber qualquer IID diferente de IID \_ IUnknown. Em sua classe derivada, teste para o IIDs de interfaces que você dá suporte, conforme mostrado no exemplo a seguir:


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



A função do utilitário [**GetInterface**](getinterface.md) (consulte [**funções auxiliares com**](com-helper-functions.md)) define o ponteiro, incrementa a contagem de referência de forma segura para thread e retorna S \_ OK. No caso padrão, chame o método da classe base e retorne o resultado. Se você derivar de outra classe base, chame seu método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) em vez disso. Isso permite que você dê suporte a todas as interfaces às quais a classe pai dá suporte.

## <a name="iunknown"></a>IUnknown

Como mencionado anteriormente, a versão de delegação de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) é a mesma para cada componente, porque não faz nada mais do que invocar a instância correta da versão que não é de delegação. Para sua conveniência, o arquivo de cabeçalho combase. h contém uma macro, [**Declare \_ IUnknown**](declare-iunknown.md), que declara os três métodos de delegação como métodos embutidos. Ele se expande para o código a seguir:


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



A função do utilitário [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do componente que possui esse componente. Para um componente agregado, o proprietário é o componente externo. Caso contrário, o componente pertence a si mesmo. Inclua a \_ macro declare IUnknown na seção pública de sua definição de classe.

## <a name="class-constructor"></a>Construtor de classe

Seu construtor de classe deve invocar o método de construtor para a classe pai, além de qualquer coisa que ele faça, seja específico para sua classe. O exemplo a seguir é um método de Construtor típico:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



O método usa os parâmetros a seguir, que passa diretamente para o método de construtor [**CUnknown**](cunknown.md) .

-   *tszName* especifica um nome para o componente.
-   *punk* é um ponteiro para o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)de agregação.
-   *PHR* é um ponteiro para um valor HRESULT, indicando o êxito ou a falha do método.

## <a name="summary"></a>Resumo

O exemplo a seguir mostra uma classe derivada que dá suporte a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e a uma interface hipotética chamada ISomeInterface:


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



Este exemplo ilustra os seguintes pontos:

-   A classe [**CUnknown**](cunknown.md) implementa a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . O novo componente herda de **CUnknown** e de quaisquer interfaces às quais o componente dá suporte. O componente pode derivar em vez de outra classe base que herda de **CUnknown**.
-   A macro [**Declare \_ IUnknown**](declare-iunknown.md) declara a delegação de métodos [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) como métodos embutidos.
-   A classe [**CUnknown**](cunknown.md) fornece a implementação para [**INonDelegatingUnknown**](inondelegatingunknown.md).
-   Para dar suporte a uma interface diferente de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), a classe derivada deve substituir o método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) e testar o IID da nova interface.
-   O construtor de classe invoca o método de construtor para [**CUnknown**](cunknown.md).

A próxima etapa na escrita de um filtro é habilitar um aplicativo para criar novas instâncias do componente. Isso requer uma compreensão das DLLs e de sua relação com as fábricas de classes e métodos de construtor de classes. para obter mais informações, consulte [como criar uma DLL de filtro de DirectShow](how-to-create-a-dll.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
