---
description: O método GetDefaultFPS recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS). Os grupos usam esse valor como a taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método IAMTimelineGroup::SetOutputFPS no grupo.
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: Método IAMTimeline::GetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 38f12abe47829544453d0aed9b8f08bffd2b5864f78fc35c873622d960387931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107846"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Método IAMTimeline::GetDefaultFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultFPS` método recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS). Os grupos usam esse valor como a taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o [**método IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) no grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFPS* 
</dt> <dd>

Recebe a taxa de quadros padrão, em quadros por segundo.

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

[**IAMTimeline Interface**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




