---
description: O método FixTimes2 agrupa os horários de início e parada especificados para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo pai. Esse método é equivalente a IAMTimelineObj::FixTimes, mas aceita valores REFTIME.
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: Método IAMTimelineObj::FixTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400901"
---
# <a name="iamtimelineobjfixtimes2-method"></a>Método IAMTimelineObj::FixTimes2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método agrupa os horários de início e parada especificados para os limites de quadro mais próximos, conforme definido pela configuração de taxa de quadros do grupo `FixTimes2` pai. Esse método é equivalente a [**IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md)mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de início, em segundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que contém a hora de parada, em segundos. Se a chamada for bem-sucedida, essa variável será definida como o tempo arredondado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou E \_ NOTINTREE se o objeto não faz parte de um grupo.

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

 

 




