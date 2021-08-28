---
description: A interface INonDeltingUnknown é uma versão de IUnknown renomeada para habilitar o suporte para interfaces IUnknown não de delegação e não de delegação no mesmo objeto COM.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: INonDeltingUnknown (Combase.h)
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
ms.openlocfilehash: f733ba28af1b4ecb7fc0a52852b4d8663fddf1df07572c409136a9aa963ba076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051606"
---
# <a name="inondelegatingunknown"></a>Inondelegatingunknown

A interface é uma versão de IUnknown renomeada para habilitar o suporte para `INonDelegatingUnknown` interfaces **IUnknown** não delegadas e não delegadas no mesmo objeto  COM.

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

Para usar `INonDelegatingUnknown` para herança múltipla, execute as etapas a seguir.

1.  Derive sua classe de uma interface, por exemplo, IMyInterface.
2.  Inclua [**DECLARE \_ IUNKNOWN em**](declare-iunknown.md) sua definição de classe para declarar implementações de **QueryInterface,** **AddRef** e **Release** que chamam o desconhecido externo.
3.  Substitua **NonDeltingQueryInterface para** expor IMyInterface com código como o seguinte:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Declare e implemente as funções membro de IMyInterface.

Para usar `INonDelegatingUnknown` para interfaces aninhadas, execute as seguintes etapas:

1.  Declare uma classe derivada de [**CUnknown**](cunknown.md).
2.  Inclua [**DECLARE \_ IUNKNOWN em**](declare-iunknown.md) sua definição de classe.
3.  Substitua **NonDeltingQueryInterface** para expor IMyInterface com o código como o seguinte:
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  Implemente as funções de membro de IMyInterface. Use [**CUnknown::GetOwner para**](cunknown-getowner.md) acessar a classe de objeto COM.
5.  Na classe de objeto COM, faça da classe aninhada um amigo da classe de objeto COM e declare uma instância da classe aninhada como membro da classe de objeto COM.

Como você sempre deve passar o desconhecido externo e um **HRESULT** para o construtor [**CUnknown,**](cunknown.md) não é possível usar um construtor padrão. Você precisa tornar a variável de membro um ponteiro para a classe e fazer uma nova chamada no construtor para realmente a criar.

Substitua **NonDeltingQueryInterface por** um código como o seguinte:


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



Você pode ter classes mistas que suportam algumas interfaces por meio de várias heranças e algumas interfaces por meio de classes aninhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções auxiliares COM**](com-helper-functions.md)
</dt> </dl>

 

 




