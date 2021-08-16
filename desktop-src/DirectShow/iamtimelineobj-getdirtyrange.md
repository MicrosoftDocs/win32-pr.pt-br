---
description: 'Método IAMTimelineObj:: GetDirtyRange-sem suporte.'
ms.assetid: 7f97b1c4-0508-45a5-a6fd-5dae17f0fa60
title: 'Método IAMTimelineObj:: GetDirtyRange (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6af9706f2a75b7d8460914bf15f6bcd7935db99539ea907b631a02b8ad94b313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400714"
---
# <a name="iamtimelineobjgetdirtyrange-method"></a>Método IAMTimelineObj:: GetDirtyRange

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Sem suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDirtyRange(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
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
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> </dl>

 

 




