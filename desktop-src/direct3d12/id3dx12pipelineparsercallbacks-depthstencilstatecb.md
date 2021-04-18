---
title: Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de estado de estêncil de profundidade de um objeto que implementa essa interface.
ms.assetid: 6E77A3B7-20D8-4D31-9D31-515CF4618157
keywords:
- Método DepthStencilStateCb
- Método DepthStencilStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método DepthStencilStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.DepthStencilStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 913dbddef0c509174d3600798a6e1380d6098808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763496"
---
# <a name="id3dx12pipelineparsercallbacks-depthstencilstatecb-method-d3dx12h"></a>Método ID3DX12PipelineParserCallbacks DepthStencilStateCb (D3DX12. h)

Chama o retorno de chamada de subobjeto de estado de estêncil de profundidade de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void DepthStencilStateCb(
  [ref] const D3D12_DEPTH_STENCIL_DESC &DepthStencilState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DepthStencilState* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ de \_ estêncil \_ de profundidade desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)**

Detalhes do subobjeto de estado de estêncil de profundidade analisado de um fluxo de estado de pipeline.

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

[**Desc. de estêncil de profundidade de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





