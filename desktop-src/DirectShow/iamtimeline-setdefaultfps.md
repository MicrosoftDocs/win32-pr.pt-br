---
description: 'O método SetDefaultFPS define a taxa de quadros de saída padrão, em quadros por segundo. Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método IAMTimelineGroup:: SetOutputFPS no grupo.'
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'Método IAMTimeline:: SetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 20c352f40234672ceeb2d4c25ea9db04e89f712d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782846"
---
# <a name="iamtimelinesetdefaultfps-method"></a>Método IAMTimeline:: SetDefaultFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetDefaultFPS` método define a taxa de quadros de saída padrão, em quadros por segundo. Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) no grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QUADROS* 
</dt> <dd>

Taxa de quadros padrão, em quadros por segundo.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




