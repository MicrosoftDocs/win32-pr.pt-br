---
description: O método GetStartStop2 recupera os horários de início e parada do objeto, em relação ao pai do objeto. Esse método é equivalente a IAMTimelineObj::GetStartStop, mas aceita valores REFTIME.
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: Método IAMTimelineObj::GetStartStop2 (Qedit.h)
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
ms.openlocfilehash: 1ff1644c2ba83848d0c9efa1b850a65aa8cfd1de1607a9fa0cabbab39579e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155444"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>Método IAMTimelineObj::GetStartStop2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método recupera os horários de início e parada do objeto, em relação ao `GetStartStop2` pai do objeto. Esse método é equivalente a [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md), mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Recebe a hora de início, em segundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recebe a hora de parada, em segundos.

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

[**IAMTimelineObj Interface**](iamtimelineobj.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




