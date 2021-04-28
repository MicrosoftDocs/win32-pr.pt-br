---
description: 'Método IAMTimelineObj:: GetDirtyRange2-sem suporte.'
ms.assetid: 3acd36f2-52f4-4734-a753-c6a6ce7e9187
title: 'Método IAMTimelineObj:: GetDirtyRange2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 14c573403bf946b54bbfcc74ae41145a3f1c5c7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119514"
---
# <a name="iamtimelineobjgetdirtyrange2-method"></a>Método IAMTimelineObj:: GetDirtyRange2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Não há suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDirtyRange2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Reservado.

</dd> <dt>

*pStop* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> </dl>

 

 




