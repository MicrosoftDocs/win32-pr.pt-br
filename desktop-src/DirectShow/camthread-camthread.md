---
description: Construtor de CAMThread. CAMThread-método de construtor.
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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096404"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




