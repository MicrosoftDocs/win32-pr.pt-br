---
description: Obtém a posição no vetor em que a alteração ocorreu.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: Método IVectorChangedEventArgs::get_Index (IVectorChangedEventArgs.h)
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
ms.openlocfilehash: 72df7f0d46e1e3073262c43064daf58b1fefbf43af913bb7f1b912ed22e67a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560642"
---
# <a name="ivectorchangedeventargsget_index-method"></a>Método IVectorChangedEventArgs::get \_ Index

Obtém a posição no vetor em que a alteração ocorreu.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Tipo: **sem \* assinatura**

A posição baseada em zero no vetor em que a alteração ocorreu, se aplicável.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                       |
| Cabeçalho<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 




