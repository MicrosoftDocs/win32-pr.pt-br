---
description: 'O método GetStartStop2 recupera as horas de início e de parada do objeto, em relação ao pai do objeto. Esse método é equivalente a IAMTimelineObj:: GetStartStop, mas usa os valores de REFTIME.'
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: 'Método IAMTimelineObj:: GetStartStop2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 211bd54ee755a08d3e592a856c792eba6e3d4e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760088"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>Método IAMTimelineObj:: GetStartStop2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetStartStop2` método recupera as horas de início e de parada do objeto, em relação ao pai do objeto. Esse método é equivalente a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md), mas usa os valores de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Recebe a hora de início, em segundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recebe a hora de parada, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




