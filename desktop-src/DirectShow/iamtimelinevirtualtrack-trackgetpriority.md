---
description: O método TrackGetPriority recupera o nível de prioridade do objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: Método IAMTimelineVirtualTrack::TrackGetPriority (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 10d84e3427cb13006cb3e674867dddb344f19a851d2afae09ad848b268e48dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051986"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a>Método IAMTimelineVirtualTrack::TrackGetPriority

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `TrackGetPriority` método recupera o nível de prioridade do objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPriority* 
</dt> <dd>

Ponteiro para uma variável que recebe o nível de prioridade. Se o objeto não for parte de uma linha do tempo, o valor será definido como -1.

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

[**IAMTimelineVirtualTrack Interface**](iamtimelinevirtualtrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




