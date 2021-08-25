---
description: O método SetStartStop2 define as horas de início e de parada do objeto, em relação ao pai do objeto. Esse método é equivalente a IAMTimelineObj::SetStartStop, mas aceita valores REFTIME.
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: Método IAMTimelineObj::SetStartStop2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 30e7f9e6ce54cb86e2eee486937841842311dd498b42ec42e101128612bf16d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086826"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>Método IAMTimelineObj::SetStartStop2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método define os horários de início e parada `SetStartStop2` do objeto, em relação ao pai do objeto. Esse método é equivalente a [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Nova hora de início, em segundos ou –1 para manter a hora de início existente.

</dd> <dt>

*Parar* 
</dt> <dd>

Nova hora de parada, em segundos ou –1 para manter a hora de parada existente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                  | Descrição                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Não implementado.<br/>  |



 

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

 

 




