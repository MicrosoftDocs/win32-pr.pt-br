---
description: Sem suporte. Em vez disso, chame o método IAMTimelineComp::GetRecursiveLayerOfType.
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: Método IAMTimelineComp::GetRecursiveLayerOfTypeI (Qedit.h)
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
ms.openlocfilehash: dc62c0813aa38af450e2f5351390ec958dddd533cc203f52b3bfb70ff45344b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756416"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a>Método IAMTimelineComp::GetRecursiveLayerOfTypeI

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Sem suporte. Em vez disso, chame o método [**IAMTimelineComp::GetRecursiveLayerOfType.**](iamtimelinecomp-getrecursivelayeroftype.md)

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

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

[**IAMTimelineComp Interface**](iamtimelinecomp.md)
</dt> </dl>

 

 




