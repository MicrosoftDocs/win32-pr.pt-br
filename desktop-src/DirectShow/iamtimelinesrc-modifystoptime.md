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
ms.openlocfilehash: f6d611395ad8989ea551fb98d1a3d538786881b0a5afc908a030367cac52ee80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952815"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK, ou E \_ INVALIDARG se a hora especificada não for válida.

## <a name="remarks"></a>Comentários

Esse método é equivalente a chamar [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) com a hora de início original e uma nova hora de parada.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




