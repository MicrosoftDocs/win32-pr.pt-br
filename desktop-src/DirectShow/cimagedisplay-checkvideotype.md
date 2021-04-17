---
description: O método CheckVideoType verifica se um formato VIDEOINFO especificado é compatível com o formato de exibição.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Método CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749014"
---
# <a name="cimagedisplaycheckvideotype-method"></a>Método CImageDisplay. CheckVideoType

O `CheckVideoType` método verifica se um formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado é compatível com o formato de exibição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInput* 
</dt> <dd>

Ponteiro para uma estrutura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se o formato for compatível ou E \_ INVALIDARG de outra forma.

## <a name="remarks"></a>Comentários

Esse método retornará S \_ OK se o tipo proposto puder ser exibido facilmente nas configurações de exibição atuais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




