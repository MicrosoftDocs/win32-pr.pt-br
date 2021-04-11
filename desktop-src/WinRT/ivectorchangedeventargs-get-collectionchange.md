---
description: Obtém o tipo de alteração que ocorreu no vetor.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Método IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164481"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>Método IVectorChangedEventArgs:: get \_ CollectionChange

Obtém o tipo de alteração que ocorreu no vetor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

Tipo: **CollectionChange \** _

Um valor da enumeração [_ *CollectionChange* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que descreve a alteração.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                       |
| parâmetro<br/>                   | <dl> <dt>IVectorChangedEventArgs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
