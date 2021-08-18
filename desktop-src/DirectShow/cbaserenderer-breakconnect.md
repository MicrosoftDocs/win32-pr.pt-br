---
description: O método BreakConnect libera o pino de entrada de uma conexão.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer.BreakConnect (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044056"
---
# <a name="cbaserendererbreakconnect-method"></a>Método CBaseRenderer.BreakConnect

O `BreakConnect` método libera o pino de entrada de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                         | Descrição                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | O pino não estava conectado.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                    |
| <dl> <dt>**VFW \_ E \_ NÃO INTERROMPIDO \_**</dt> </dl> | O filtro ainda está ativo.<br/> |



 

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método de dentro de seu `BreakConnect` próprio método. (Para obter mais informações, [**consulte CBasePin::BreakConnect**](cbasepin-breakconnect.md).) O filtro executa alguma contabilidade interna, como redefinir o sinalizador de fim do fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




