---
description: 'Não há suporte. Em vez disso, chame o método IAMTimelineComp:: GetRecursiveLayerOfType.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Método IAMTimelineComp:: GetRecursiveLayerOfTypeI (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759446"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Método IAMTimelineComp:: GetRecursiveLayerOfTypeI

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Não há suporte. Em vez disso, chame o método [**IAMTimelineComp:: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVirtualTrack* 
</dt> <dd>

Reservado.

</dd> <dt>

*pWhichLayer* 
</dt> <dd>

Reservado.

</dd> <dt>

*Tipo* 
</dt> <dd>

Reservado.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> </dl>

 

 




