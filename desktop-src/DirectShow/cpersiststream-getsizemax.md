---
description: Recupera o tamanho máximo de bytes necessário para o fluxo atual, incluindo o número de versão.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Método CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756616"
---
# <a name="cpersiststreamgetsizemax-method"></a>Método CPersistStream. GetSizeMax

Recupera o tamanho máximo de bytes necessário para o fluxo atual, incluindo o número de versão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcbSize* 
</dt> <dd>

Ponteiro para o tamanho em bytes necessário para salvar este fluxo, incluindo o número de versão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método **IPersistStream:: GetSizeMax** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




