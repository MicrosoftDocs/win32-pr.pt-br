---
description: O método CheckStreaming determina se o pino pode aceitar exemplos.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Método CTransformInputPin.CheckStreaming (Transfrm.h)
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
ms.openlocfilehash: c32dce44e48b033e0a76f5bb5af6aff3eb71948d54c73d670c6226571a1c938b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767602"
---
# <a name="ctransforminputpincheckstreaming-method"></a>Método CTransformInputPin.CheckStreaming

O `CheckStreaming` método determina se o pino pode aceitar exemplos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | O pino está sendo liberado no momento.<br/>       |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino de saída não está conectado.<br/> |
| <dl> <dt>**ERRO DE \_ \_ RUNTIME DO VFW E \_**</dt> </dl> | Ocorreu um erro em tempo de run time.<br/>       |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ ERRADO**</dt> </dl>   | O pino é interrompido.<br/>              |



 

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBaseInputPin::CheckStreaming.**](cbaseinputpin-checkstreaming.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




