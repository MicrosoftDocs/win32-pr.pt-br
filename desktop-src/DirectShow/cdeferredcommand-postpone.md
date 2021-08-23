---
description: O método adiado especifica um novo tempo de apresentação para um comando anteriormente enfileirado.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Método CDeferredCommand. adie (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074360"
---
# <a name="cdeferredcommandpostpone-method"></a>Método CDeferredCommand. adie

O `Postpone` método especifica um novo tempo de apresentação para um comando enfileirado anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newtime* 
</dt> <dd>

Nova hora da apresentação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará VFW \_ E \_ hora \_ já \_ passado se *Newtime* já tiver passado. Caso contrário, retorna um **HRESULT** resultante de uma chamada para [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (ao extrair da lista) ou [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (ao reinserir com o tempo alterado).

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




