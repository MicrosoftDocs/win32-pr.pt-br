---
title: Método PrimitiveTopologyTypeCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chama o retorno de chamada de subobjeto do tipo topologia primitivo de um objeto que implementa essa interface.
ms.assetid: FF9D8D5C-3A6A-40D8-8EA4-3EA305EB4568
keywords:
- Método PrimitiveTopologyTypeCb
- Método PrimitiveTopologyTypeCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método PrimitiveTopologyTypeCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.PrimitiveTopologyTypeCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e67f7d3c6805c411222e6e4202e21d2f31ced78211fb364829e7ace2dac2ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807226"
---
# <a name="id3dx12pipelineparsercallbacksprimitivetopologytypecb-method"></a>Método ID3DX12PipelineParserCallbacks::P rimitiveTopologyTypeCb

Chama o retorno de chamada de subobjeto do tipo topologia primitivo de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void PrimitiveTopologyTypeCb(
   D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PrimitiveTopologyType* 
</dt> <dd>

Tipo: **[ **TIPO DE \_ \_ TOPOLOGIA \_ PRIMITIVA D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)**

Detalhes do subobjeto de tipo de topologia primitivo analisado de um fluxo de estado de pipeline.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não retorna nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces auxiliares para Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> <dt>

[**TIPO DE \_ TOPOLOGIA PRIMITIVA D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)
</dt> </dl>

 

 





