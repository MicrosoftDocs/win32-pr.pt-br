---
description: Obtém a posição no vetor em que a alteração ocorreu.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'Método IVectorChangedEventArgs:: get_Index (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010496"
---
# <a name="ivectorchangedeventargsget_index-method"></a>Método de índice IVectorChangedEventArgs:: get \_

Obtém a posição no vetor em que a alteração ocorreu.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

Tipo: **não assinado \** _

A posição de base zero no vetor em que a alteração ocorreu, se aplicável.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

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

 

 




