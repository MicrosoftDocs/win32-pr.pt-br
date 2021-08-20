---
description: O método AllocFormatBuffer aloca memória para o bloco de formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Método CMediaType.AllocFormatBuffer (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073980"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Método CMediaType.AllocFormatBuffer

O `AllocFormatBuffer` método aloca memória para o bloco de formato.

## <a name="syntax"></a>Sintaxe


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*length* 
</dt> <dd>

Tamanho necessário para o bloco de formato, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o novo bloco se for bem-sucedido. Caso contrário, **retornará NULL.**

## <a name="remarks"></a>Comentários

Se o método alocar com êxito um novo bloco de formato, ele liberará o bloco de formato existente. Se a alocação falhar, o método deixará o bloco de formato existente.

O método atualiza os **membros cbFormat** e **pbFormat** da estrutura **AM MEDIA \_ \_ TYPE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




