---
description: O método TrackGetPriority recupera o nível de prioridade do objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Método IAMTimelineVirtualTrack:: TrackGetPriority (QEdit. h)'
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
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760084"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a>Método IAMTimelineVirtualTrack:: TrackGetPriority

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

Ponteiro para uma variável que recebe o nível de prioridade. Se o objeto não fizer parte de uma linha do tempo, o valor será definido como – 1.

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

[**Interface IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




