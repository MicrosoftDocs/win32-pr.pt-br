---
description: Sinalizador que indica se ocorreu um erro em tempo de execução.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membro CBasePin:: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752903"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Membro de CBasePin:: m \_ bRunTimeError

Sinalizador que indica se ocorreu um erro em tempo de execução.

## <a name="syntax"></a>Sintaxe


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Comentários

Esse sinalizador assume como padrão **false**. Defina o sinalizador como **verdadeiro** se ocorrer um erro em tempo de execução durante o streaming. O método [**CBasePin:: Inactive**](cbasepin-inactive.md) redefine o sinalizador como **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




