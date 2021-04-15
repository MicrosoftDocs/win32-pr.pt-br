---
description: O método CoInitializeHelper chama a função CoInitializeEx no início do thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753761"
---
# <a name="camthreadcoinitializehelper-method"></a>Método CAMThread. CoInitializeHelper

O `CoInitializeHelper` método chama a função CoInitializeEx no início do thread.

## <a name="syntax"></a>Sintaxe


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores a seguir são possíveis.



| Código de retorno                                                                             | Descrição                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | A função CoInitializeEx não está disponível.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                      |
| <dl> <dt>**E \_ falha**</dt> </dl>  | Falha.<br/>                                      |



 

## <a name="remarks"></a>Comentários

O método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) chama esse método auxiliar, que chama a função CoInitializeEx. Ele usa o sinalizador de \_ desabilitar OLE1DDE do coinit \_ para desabilitar o troca dinâmica de dados (DDE). Para obter mais informações, consulte o SDK da plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




