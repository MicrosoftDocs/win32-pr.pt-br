---
description: 'O método GetDefaultFPS recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS). Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método IAMTimelineGroup:: SetOutputFPS no grupo.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Método IAMTimeline:: GetDefaultFPS (QEdit. h)'
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
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757295"
---
# <a name="iamtimelinegetdefaultfps-method"></a>Método IAMTimeline:: GetDefaultFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetDefaultFPS` método recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS). Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) no grupo.

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

 

 




