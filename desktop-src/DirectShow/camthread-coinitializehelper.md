---
description: O método CoInitializeHelper chama a função CoInitializeEx no início do thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread.CoInitializeHelper (Wxutil.h)
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
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768286"
---
# <a name="camthreadcoinitializehelper-method"></a>Método CAMThread.CoInitializeHelper

O `CoInitializeHelper` método chama a função CoInitializeEx no início do thread.

## <a name="syntax"></a>Sintaxe


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** A seguir estão os valores possíveis.



| Código de retorno                                                                             | Descrição                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | A função CoInitializeEx não está disponível.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Falha.<br/>                                      |



 

## <a name="remarks"></a>Comentários

O [**método CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) chama esse método auxiliar, que chama a função CoInitializeEx. Ele usa o sinalizador COINIT \_ DISABLE \_ OLE1DDE para desabilitar Dados Dinâmicos Exchange (DDE). Para obter mais informações, consulte o SDK da plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




