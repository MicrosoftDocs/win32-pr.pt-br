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
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504806"
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

Tipo: **CollectionChange \***

Um valor da enumeração [**CollectionChange**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) que descreve a alteração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>IVectorChangedEventArgs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
