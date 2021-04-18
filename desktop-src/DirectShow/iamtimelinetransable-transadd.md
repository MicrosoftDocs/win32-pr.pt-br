---
description: O método TransAdd adiciona uma transição para o objeto. Um objeto pode ter várias transições, mas eles não devem se sobrepor no tempo. As transições devem estar dentro dos limites de tempo do objeto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'Método IAMTimelineTransable:: TransAdd (QEdit. h)'
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
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779843"
---
# <a name="iamtimelinetransabletransadd-method"></a>Método IAMTimelineTransable:: TransAdd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `TransAdd` método adiciona uma transição para o objeto. Um objeto pode ter várias transições, mas eles não devem se sobrepor no tempo. As transições devem estar dentro dos limites de tempo do objeto.

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

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição a ser adicionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                   | Descrição                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Não é possível inserir a transição.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *pTrans* não é um ponteiro para uma transição.<br/> |



 

## <a name="remarks"></a>Comentários

Se a transição sobrepor uma transição existente, o método retornará E \_ INVALIDARG.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




