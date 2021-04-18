---
description: O método ShouldUpdate determina se é necessário criar uma nova paleta.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Método CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756599"
---
# <a name="cimagepaletteshouldupdate-method"></a>Método CImagePalette. ShouldUpdate

O `ShouldUpdate` método determina se é necessário criar uma nova paleta.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNewInfo* 
</dt> <dd>

Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém a nova tabela de cores.

</dd> <dt>

*pOldInfo* 
</dt> <dd>

Ponteiro para uma estrutura **VIDEOINFOHEADER** que contém a tabela de cores antiga. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a paleta precisar ser atualizada ou **false** caso contrário.

## <a name="remarks"></a>Comentários

-   Se nenhuma estrutura **VIDEOINFOHEADER** contiver uma tabela de cores, o método retornará **false**.
-   Se apenas uma estrutura contiver uma tabela de cores ou se *pOldInfo* for **NULL**, o método retornará **true**.
-   Se ambas as estruturas contiverem tabelas de cores e as entradas de cor corresponderem, o método retornará **false**.
-   Se ambas as estruturas contiverem tabelas de cores, mas as entradas de cor não corresponderem, o método retornará **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




