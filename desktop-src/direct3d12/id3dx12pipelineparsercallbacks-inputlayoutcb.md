---
title: Método ID3DX12PipelineParserCallbacks InputLayoutCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de layout de entrada de um objeto que implementa essa interface.
ms.assetid: A21AB7A1-6E51-42CB-BA98-C0BD08D43009
keywords:
- Método InputLayoutCb
- Método InputLayoutCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método InputLayoutCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.InputLayoutCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f7012686c85b38e94f8f3d2400cf406d614fc83ff0ba25e746ac0433b2e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528768"
---
# <a name="id3dx12pipelineparsercallbacksinputlayoutcb-method"></a>Método ID3DX12PipelineParserCallbacks:: InputLayoutCb

Chama o retorno de chamada de subobjeto de layout de entrada de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void InputLayoutCb(
  [ref] const D3D12_INPUT_LAYOUT_DESC &InputLayout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*InputLayout* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ layout de entrada \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)**

Detalhes do subobjeto de layout de entrada analisado de um fluxo de estado de pipeline.

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

[**D3D12 \_ de \_ layout de entrada \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc)
</dt> </dl>

 

 





