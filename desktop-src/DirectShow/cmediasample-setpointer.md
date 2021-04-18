---
description: O método SetPointer define o ponteiro para o buffer de memória.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Método CMediaSample. setpointr (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779553"
---
# <a name="cmediasamplesetpointer-method"></a>Método CMediaSample. setpointr

O `SetPointer` método define o ponteiro para o buffer de memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptr* 
</dt> <dd>

Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *cBytes*.

</dd> <dt>

*cBytes* 
</dt> <dd>

Comprimento do buffer, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método permite que o alocador defina um novo ponteiro para o exemplo.

Esse método não está disponível por meio da interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . O objeto que cria o exemplo pode acessar esse método (por meio de **CMediaSample**), mas outros objetos não podem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




