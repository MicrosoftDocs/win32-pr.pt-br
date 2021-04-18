---
description: O método ModifyStopTime define a hora de parada, em relação à linha do tempo.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'Método IAMTimelineSrc:: ModifyStopTime (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786974"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>Método IAMTimelineSrc:: ModifyStopTime

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ModifyStopTime` método define a hora de parada, em relação à linha do tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Parar* 
</dt> <dd>

Nova hora de parada, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK, ou E \_ INVALIDARG se a hora especificada não for válida.

## <a name="remarks"></a>Comentários

Esse método é equivalente a chamar [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) com a hora de início original e uma nova hora de parada.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




