---
description: 'CFactoryTemplate:: m_lpfnNew ponteiro de membro para uma função que cria uma instância do objeto.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Membro CFactoryTemplate:: m_lpfnNew (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a08b0f1b3dc28b70e62866b58a952b12959f0a7f753d5e6b4c847489b52bfd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317716"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>Membro de CFactoryTemplate:: m \_ lpfnNew

Ponteiro para uma função que cria uma instância do objeto.

## <a name="syntax"></a>Sintaxe


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Comentários

Em sua DLL, declare uma função estática que retorna um ponteiro para uma nova instância do objeto. No modelo de fábrica, defina a variável de membro **m \_ lpfnNew** como o endereço dessa função estática.

O tipo de ponteiro de função é [**LPFNNewCOMObject**](lpfnnewcomobject.md).

O exemplo a seguir mostra uma função típica para **m \_ lpfnNew**:


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




