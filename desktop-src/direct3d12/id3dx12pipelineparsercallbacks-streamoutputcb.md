---
title: Método ID3DX12PipelineParserCallbacks StreamOutputCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.
ms.assetid: 93447ABE-A942-4562-A532-600EC63072DA
keywords:
- Método StreamOutputCb
- Método StreamOutputCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método StreamOutputCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.StreamOutputCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae32f084edd2b6af374aa9b1cac4e563ef8a2eb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791341"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Método ID3DX12PipelineParserCallbacks:: StreamOutputCb

Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StreamOutput* \[ referência\]
</dt> <dd>

Tipo: **const [**D3D12 \_ saída de fluxo \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Detalhes do subobjeto de descrição de saída do fluxo analisado a partir de um fluxo de estado do pipeline.

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

[**\_Desc de \_ saída de fluxo D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





