---
description: O método TransAdd adiciona uma transição ao objeto . Um objeto pode ter várias transições, mas não deve se sobrepor no tempo. As transições devem estar dentro dos limites de tempo do objeto .
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: Método IAMTimelineTransable::TransAdd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 930c3ff43e11cfb71ffce6c7257d0124fe87aeaaf4ae065433f11b860020eeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952745"
---
# <a name="iamtimelinetransabletransadd-method"></a>Método IAMTimelineTransable::TransAdd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `TransAdd` método adiciona uma transição para o objeto . Um objeto pode ter várias transições, mas não deve se sobrepor no tempo. As transições devem estar dentro dos limites de tempo do objeto .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTrans* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição a ser acrescentada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                   | Descrição                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Não é possível inserir a transição.<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *pTrans* não é um ponteiro para uma transição.<br/> |



 

## <a name="remarks"></a>Comentários

Se a transição se sobrepor a uma transição existente, o método retornará E \_ INVALIDARG.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineTransable Interface**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




