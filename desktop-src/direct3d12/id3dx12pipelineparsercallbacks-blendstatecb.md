---
title: Método ID3DX12PipelineParserCallbacks BlendStateCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de estado de mesclagem de um objeto que implementa essa interface.
ms.assetid: C00C733B-4123-4795-9A93-973F30BE456B
keywords:
- Método BlendStateCb
- Método BlendStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método BlendStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.BlendStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 119733fbe82203a6e423fb0ef9b07d3ecff70619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780260"
---
# <a name="id3dx12pipelineparsercallbacksblendstatecb-method"></a>Método ID3DX12PipelineParserCallbacks:: BlendStateCb

Chama o retorno de chamada de subobjeto de descrição de estado de mesclagem de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void BlendStateCb(
  [ref] const D3D12_BLEND_DESC &BlendState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Blendstate* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)**

Detalhes do subobjeto de descrição do estado de mesclagem analisado a partir de um fluxo de estado do pipeline.

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
</dt> <dt>

[**D3D12 de \_ combinação \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> </dl>

 

 





