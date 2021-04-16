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
ms.openlocfilehash: 5181e8d9fb83b7338adc3af5c0ce44aec1b447d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808208"
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

## <a name="return-value"></a>Retornar valor

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

 

 





