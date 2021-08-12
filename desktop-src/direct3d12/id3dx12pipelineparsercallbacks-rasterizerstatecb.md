---
title: Método ID3DX12PipelineParserCallbacks RasterizerStateCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de estado do rasterizador de um objeto que implementa essa interface.
ms.assetid: 125FC6EC-B749-4EE2-9D34-14BD12993BDC
keywords:
- Método RasterizerStateCb
- Método RasterizerStateCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método RasterizerStateCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.RasterizerStateCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a179f26d88f25027eb9ffc2b4b3712ac963b65179334fff1bfa4d6103ef76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528616"
---
# <a name="id3dx12pipelineparsercallbacksrasterizerstatecb-method"></a>Método ID3DX12PipelineParserCallbacks:: RasterizerStateCb

Chama o retorno de chamada de subobjeto de descrição de estado do rasterizador de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void RasterizerStateCb(
  [ref] const D3D12_RASTERIZER_DESC &RasterizerState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RasterizerState* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ rasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**

Detalhes do subobjeto de descrição do estado do rasterizador analisado a partir de um fluxo de estado do pipeline.

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
</dt> <dt>

[**D3D12 do \_ rasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> </dl>

 

 





