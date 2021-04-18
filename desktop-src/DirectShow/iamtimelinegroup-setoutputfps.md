---
description: O método SetOutputFPS define a taxa de quadros de saída não compactados para esse grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Método IAMTimelineGroup:: SetOutputFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760089"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Método IAMTimelineGroup:: SetOutputFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetOutputFPS` método define a taxa de quadros de saída não compactados para esse grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*QUADROS* 
</dt> <dd>

Taxa de quadros de saída para este grupo, em quadros por segundo. O valor não pode ser igual a zero e não pode ter mais de sete dígitos após a casa decimal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A saída renderizada desse grupo é executada na taxa de quadros especificada e todas as edições no material de origem são arredondadas para o limite de quadro mais próximo, conforme definido pela taxa de quadros. Para obter o melhor desempenho, use a mesma taxa de quadros para todos os grupos, vídeo e áudio.

O método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) substitui a taxa de quadros.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




