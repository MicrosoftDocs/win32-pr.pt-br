---
description: A interface INonDelegatingUnknown é uma versão de IUnknown que é renomeada para habilitar o suporte para interfaces de não delegação e de delegação de interface IUnknown no mesmo objeto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDelegatingUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775602"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

A `INonDelegatingUnknown` interface é uma versão de **IUnknown** renomeada para habilitar o suporte para interfaces de não delegação e de delegação de interface **IUnknown** no mesmo objeto com.

## <a name="syntax"></a>Sintaxe


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>Comentários

Para usar `INonDelegatingUnknown` para várias heranças, execute as etapas a seguir.

1.  Derive sua classe de uma interface, por exemplo, IMinhaInterface.
2.  Inclua [**Declare \_ IUnknown**](declare-iunknown.md) em sua definição de classe para declarar implementações de **QueryInterface**, **AddRef** e **Release** que chamam o desconhecido externo.
3.  Substitua **NonDelegatingQueryInterface** para expor IMinhaInterface com código como o seguinte:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Declare e implemente as funções de membro de IMinhaInterface.

Para usar `INonDelegatingUnknown` o para interfaces aninhadas, execute as seguintes etapas:

1.  Declare uma classe derivada de [**CUnknown**](cunknown.md).
2.  Inclua [**Declare \_ IUnknown**](declare-iunknown.md) em sua definição de classe.
3.  Substitua **NonDelegatingQueryInterface** para expor IMinhaInterface com o código como o seguinte:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implemente as funções de membro de IMinhaInterface. Use [**CUnknown:: GetOwner**](cunknown-getowner.md) para acessar a classe de objeto com.
5.  Em sua classe de objeto COM, torne a classe aninhada um amigo da classe de objeto COM e declare uma instância da classe aninhada como um membro da classe de objeto COM.

Como você sempre deve passar o desconhecido externo e um **HRESULT** para o construtor [**CUnknown**](cunknown.md) , não é possível usar um construtor padrão. Você precisa tornar a variável de membro um ponteiro para a classe e fazer uma nova chamada em seu construtor para realmente criá-la.

Substitua o **NonDelegatingQueryInterface** por um código como o seguinte:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Você pode ter classes mistas que dão suporte a algumas interfaces por meio de várias heranças e algumas interfaces por meio de classes aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 




