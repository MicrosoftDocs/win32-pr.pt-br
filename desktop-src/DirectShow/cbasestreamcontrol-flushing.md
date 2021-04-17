---
description: O método de liberação notifica a classe base de que o PIN foi iniciado ou parou de ser liberado.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Método CBaseStreamControl. Flushing (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754993"
---
# <a name="cbasestreamcontrolflushing-method"></a>Método CBaseStreamControl. Flushing

O `Flushing` método notifica a classe base de que o PIN foi iniciado ou parou de ser liberado.

## <a name="syntax"></a>Sintaxe


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bInProgress* 
</dt> <dd>

Especifica um valor booliano que indica se o PIN está sendo liberado. Use o valor **true** quando o PIN iniciar uma operação de liberação e **false** quando o PIN terminar uma operação de liberação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O PIN deve chamar esse método de dentro dos métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) . Especifique **true** em **BeginFlush** e **false** em **EndFlush**.

Esse método faz com que o método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) pare de esperar. Enquanto o PIN está sendo liberado, **CheckStreamState** sempre retorna a \_ descartação de fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




