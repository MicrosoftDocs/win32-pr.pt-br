---
description: O método ChangeRate é chamado quando a taxa de reprodução é muda.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Método CSourceSeeking.ChangeRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee74c8eb39fbebab1e58442c3b12f8342610ed792f4eb80ee70e5f44c3cca236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633936"
---
# <a name="csourceseekingchangerate-method"></a>Método CSourceSeeking.ChangeRate

O `ChangeRate` método é chamado quando a taxa de reprodução é muda.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

O [**método CSourceSeeking::SetRate**](csourceseeking-setrate.md) chama esse método, que a classe derivada deve implementar. O **método SetRate** atualiza a variável de membro [**CSourceSeeking::m \_ dRateSeeking,**](csourceseeking-m-drateseeking.md) mas não valida o novo valor. Uma taxa de zero sempre deve ser rejeitada. Taxas menores que zero indicam reprodução negativa. A maioria dos filtros não é suportada por taxas negativas.

O exemplo a seguir mostra uma implementação possível:


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




