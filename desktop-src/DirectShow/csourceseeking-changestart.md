---
description: O método altere é chamado quando a posição inicial é alterada.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Método CSourceSeeking. Altere (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747815"
---
# <a name="csourceseekingchangestart-method"></a>Método CSourceSeeking. Altere

O `ChangeStart` método é chamado quando a posição inicial é alterada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CSourceSeeking:: Setposicionations**](csourceseeking-setpositions.md) chamará esse método se a posição inicial for alterada. Este método é virtual puro; a classe derivada deve implementá-la. Após uma operação de busca, os carimbos de data/hora devem reiniciar de zero. Os horários de mídia devem refletir a nova hora de início. O exemplo a seguir mostra uma possível implementação:


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
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

 

 




