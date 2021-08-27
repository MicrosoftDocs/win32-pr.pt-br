---
description: O método SetFormat Inicializa o bloco de formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Método CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108446"
---
# <a name="cmediatypesetformat-method"></a>Método CMediaType. SetFormat

O `SetFormat` método inicializa o bloco de formato.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Ponteiro para um bloco de memória que contém o bloco de formato.

</dd> <dt>

*length* 
</dt> <dd>

Comprimento do bloco de formato, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro.

## <a name="remarks"></a>Comentários

Esse método aloca memória para o bloco de formato e copia o buffer especificado por *pFormat* no novo bloco de formato. Se o tipo de mídia já contiver um bloco de formato, o antigo será liberado. O método também define o membro **cbFormat** da estrutura **do \_ \_ tipo de mídia am** .

Para definir o tipo de formato, chame o método [**CMediaType:: Setformattype**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




