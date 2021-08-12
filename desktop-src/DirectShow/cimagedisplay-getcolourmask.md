---
description: O método GetColourMask recupera as máscaras de cores para o formato de exibição atual.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Método CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 018bdaf96e5b6508e13893290449d77041c453b3b28bb4c4d794cc5cc85fb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655937"
---
# <a name="cimagedisplaygetcolourmask-method"></a>Método CImageDisplay. GetColourMask

O `GetColourMask` método recupera as máscaras de cores para o formato de exibição atual.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMaskRed* 
</dt> <dd>

Ponteiro para uma variável que recebe a máscara de componente vermelho.

</dd> <dt>

*pMaskGreen* 
</dt> <dd>

Ponteiro para uma variável que recebe a máscara de componente verde.

</dd> <dt>

*pMaskBlue* 
</dt> <dd>

Ponteiro para uma variável que recebe a máscara de componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




