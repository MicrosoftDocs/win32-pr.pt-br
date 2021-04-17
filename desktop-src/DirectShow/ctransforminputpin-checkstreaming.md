---
description: O método CheckStreaming determina se o PIN pode aceitar amostras.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Método CTransformInputPin. CheckStreaming (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748190"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Método CTransformInputPin. CheckStreaming

O `CheckStreaming` método determina se o PIN pode aceitar amostras.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                         |
| <dl> <dt>**\_falso**</dt> </dl>               | O PIN está sendo liberado no momento.<br/>       |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O pino de saída não está conectado.<br/> |
| <dl> <dt>**VFW \_ E \_ erro de tempo de execução \_**</dt> </dl> | Ocorreu um erro em tempo de execução.<br/>       |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>   | O PIN foi interrompido.<br/>              |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseInputPin:: CheckStreaming**](cbaseinputpin-checkstreaming.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




