---
description: Construtor CAMThread.CAMThread – método do construtor.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Construtor CAMThread.CAMThread (Wxutil.h)
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
ms.openlocfilehash: e042624573cd0c421e8ecd202cde971a49eef95cc5f3c6c0ac64bf45b4cf9c19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103326"
---
# <a name="camthreadcamthread-constructor"></a>Construtor CAMThread.CAMThread

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **valor HRESULT.** Se o construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

Para compatibilidade com versões anteriores do strmbase.lib, esse parâmetro assume null como **padrão.** No entanto, é preferível passar **um valor** não NULL para que o chamador possa verificar o status do objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método do construtor não cria o thread. Para criar o thread, chame o [**método CAMThread::Create.**](camthread-create.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




