---
description: 'O método ModifyStopTime2 define a hora de parada. Esse método é equivalente a IAMTimelineSrc:: ModifyStopTime, mas usa um valor de REFTIME.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'Método IAMTimelineSrc:: ModifyStopTime2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779850"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Método IAMTimelineSrc:: ModifyStopTime2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ModifyStopTime2` método define a hora de parada. Esse método é equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), mas usa um valor de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Parar* 
</dt> <dd>

Nova hora de parada, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido, ou E \_ INVALIDARG se a hora especificada não for válida.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




