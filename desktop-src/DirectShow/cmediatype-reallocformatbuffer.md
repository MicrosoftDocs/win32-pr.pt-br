---
description: O método ReallocFormatBuffer realoca o bloco de formato para um novo tamanho.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType. ReallocFormatBuffer (mtype. h)
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
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771851"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Método CMediaType. ReallocFormatBuffer

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

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para o novo bloco se for bem-sucedido. Caso contrário, retorna um ponteiro para o bloco de formato antigo ou **NULL**.

## <a name="remarks"></a>Comentários

Esse método aloca um novo bloco de formato. Ele copia o máximo possível de bloco de formato existente no novo bloco de formato. Se o novo bloco for menor do que o bloco existente, o bloco de formato existente será truncado. Se o novo bloco for maior, o conteúdo do espaço adicional será indefinido. Eles não são definidos explicitamente como zero.

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

 

 




