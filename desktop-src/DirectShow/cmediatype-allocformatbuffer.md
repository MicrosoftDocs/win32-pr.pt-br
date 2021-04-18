---
description: O método AllocFormatBuffer aloca memória para o bloco de formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Método CMediaType. AllocFormatBuffer (mtype. h)
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
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750474"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Método CMediaType. AllocFormatBuffer

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

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para o novo bloco se for bem-sucedido. Caso contrário, retornará **NULL**.

## <a name="remarks"></a>Comentários

Se o método alocar um novo bloco de formato com êxito, ele liberará o bloco de formato existente. Se a alocação falhar, o método deixará o bloco de formato existente.

O método atualiza os membros **cbFormat** e **pbFormat** da estrutura **do \_ \_ tipo de mídia am** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




