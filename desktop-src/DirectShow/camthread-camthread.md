---
description: Método de construtor.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Construtor CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756001"
---
# <a name="camthreadcamthread-constructor"></a>Construtor CAMThread. CAMThread

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Se o Construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão. No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método de construtor não cria o thread. Para criar o thread, chame o método [**CAMThread:: Create**](camthread-create.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




