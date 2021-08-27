---
title: Método ID3DX12PipelineParserCallbacks ErrorBadInputParameter (D3DX12. h)
description: Chama o retorno de chamada de erro de parâmetro de entrada inadequado de um objeto que implementa essa interface.
ms.assetid: CB1F9A77-B120-4D72-99D3-16594E668520
keywords:
- Método ErrorBadInputParameter
- Método ErrorBadInputParameter, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método ErrorBadInputParameter
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorBadInputParameter
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fb00490fc2c2710207e7bdd01f7be900996452f34b379a2c883ef2a99dfcd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096408"
---
# <a name="id3dx12pipelineparsercallbackserrorbadinputparameter-method"></a>Método ID3DX12PipelineParserCallbacks:: ErrorBadInputParameter

Chama o retorno de chamada de erro de parâmetro de entrada inadequado de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void ErrorBadInputParameter(
   
        UINT
           ParameterIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ParameterIndex* 
</dt> <dd>

Tipo: **uint**

A posição do parâmetro que contém entrada inadequada. O parâmetro mais à esquerda está na posição 1, não na posição 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não retorna nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





