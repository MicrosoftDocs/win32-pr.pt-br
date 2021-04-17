---
description: O método de redefinição redefine o objeto para que ele possa receber mais dados.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Método COutputQueue. Reset (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754259"
---
# <a name="coutputqueuereset-method"></a>Método COutputQueue. Reset

O `Reset` método redefine o objeto para que ele possa receber mais dados.

## <a name="syntax"></a>Sintaxe


```C++
void Reset();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método redefine a variável de membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) para S \_ OK. O objeto pode receber amostras de mídia novamente; por exemplo, após uma operação de liberação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




