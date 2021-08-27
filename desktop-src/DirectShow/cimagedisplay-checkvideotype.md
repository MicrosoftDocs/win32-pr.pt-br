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
ms.openlocfilehash: de6389e22868fe529b5038fe6be1403748dd5a01d22a242c41f9e6c6b8f86808
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108486"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se o formato for compatível ou E \_ INVALIDARG de outra forma.

## <a name="remarks"></a>Comentários

Esse método retornará S \_ OK se o tipo proposto puder ser exibido facilmente nas configurações de exibição atuais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




