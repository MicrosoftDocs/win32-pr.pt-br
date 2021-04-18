---
description: O método UnblockOutputPin desbloqueia o PIN. Quando o PIN é desbloqueado, ele pode entregar amostras, alterar seu formato de saída e se conectar novamente.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Método CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778625"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a>Método CDynamicOutputPin. UnblockOutputPin

O `UnblockOutputPin` método desbloqueia o PIN. Quando o PIN é desbloqueado, ele pode entregar amostras, alterar seu formato de saída e se conectar novamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN já estava desbloqueado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




