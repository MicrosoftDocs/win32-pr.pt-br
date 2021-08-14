---
description: O método ModifyStopTime2 define a hora de parada. Esse método é equivalente a IAMTimelineSrc::ModifyStopTime, mas aceita um valor REFTIME.
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: Método IAMTimelineSrc::ModifyStopTime2 (Qedit.h)
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
ms.openlocfilehash: fa2ec7a019200f91c9fb2a894c978ce93896926024f55efb229c7e5fde6fbe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952805"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>Método IAMTimelineSrc::ModifyStopTime2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ModifyStopTime2` método define a hora de parada. Esse método é equivalente a [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), mas obtém um [**valor REFTIME.**](reftime.md)

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

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou E \_ INVALIDARG se a hora especificada não for válida.

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

[**IAMTimelineSrc Interface**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




