---
description: O método setformatype especifica o tipo de formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Método CMediaType. setformattype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780866"
---
# <a name="cmediatypesetformattype-method"></a>Método CMediaType. setformatype

O método setformattype especifica o tipo de formato.

## <a name="syntax"></a>Sintaxe


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pformattype* 
</dt> <dd>

Ponteiro para um **GUID** que especifica o tipo de formato.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define o membro **formatType** . O tipo de formato define o layout do bloco de formato. Por exemplo, se o tipo de formato for FORMAT \_ VIDEOINFO, o bloco de formato deverá conter uma estrutura **VIDEOINFOHEADER** . Para definir o bloco de formato, chame o método [**CMediaType:: SetFormat**](cmediatype-setformat.md) . O chamador é responsável por verificar se o bloco de formato corresponde ao tipo de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 


``
