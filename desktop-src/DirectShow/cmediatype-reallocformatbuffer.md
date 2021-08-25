---
description: O método ReallocFormatBuffer realoca o bloco de formato para um novo tamanho.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType.ReallocFormatBuffer (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bd4d7bd27c3698f1e30c690f755f445ffaffeff37c88f27d0a5c8ba58cd2d32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768166"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Método CMediaType.ReallocFormatBuffer

O `ReallocFormatBuffer` método realoca o bloco de formato para um novo tamanho.

## <a name="syntax"></a>Sintaxe


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*length* 
</dt> <dd>

Novo tamanho necessário para o bloco de formato, em bytes. Deve ser maior que zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para o novo bloco se for bem-sucedido. Caso contrário, retornará um ponteiro para o bloco de formato antigo ou **NULL.**

## <a name="remarks"></a>Comentários

Esse método aloca um novo bloco de formato. Ele copia o máximo possível do bloco de formato existente para o novo bloco de formato. Se o novo bloco for menor que o bloco existente, o bloco de formato existente será truncado. Se o novo bloco for maior, o conteúdo do espaço adicional será indefinido. Eles não são definidos explicitamente como zero.

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

 

 




