---
description: O método de trocador é chamado quando a taxa de reprodução é alterada.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Método CSourceSeeking. Disqueteiraize (Ctlutil. h)
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
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782852"
---
# <a name="csourceseekingchangerate-method"></a>Método CSourceSeeking. peralterador

O `ChangeRate` método é chamado quando a taxa de reprodução é alterada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) chama esse método, que a classe derivada deve implementar. O método **SetRate** atualiza a variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , mas não valida o novo valor. Uma taxa de zero sempre deve ser rejeitada. Taxas menores que zero indicam reprodução negativa. A maioria dos filtros não oferece suporte a taxas negativas.

O exemplo a seguir mostra uma possível implementação:


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
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




