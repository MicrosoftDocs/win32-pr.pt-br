---
title: Método StreamOutputCb ID3DX12PipelineParserCallbacks (D3DX12.h)
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
ms.openlocfilehash: f1e484d044bc4de2be3d40c6080e77b62aa57b59f0161c2021b8696316970542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632346"
---
# <a name="id3dx12pipelineparsercallbacksstreamoutputcb-method"></a>Método ID3DX12PipelineParserCallbacks::StreamOutputCb

Chama o retorno de chamada de subobjeto de descrição de saída de fluxo de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void StreamOutputCb(
  [ref] const D3D12_STREAM_OUTPUT_DESC &StreamOutput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StreamOutput* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ STREAM OUTPUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)**

Detalhes do subobjeto de descrição da saída do fluxo analisado de um fluxo de estado do pipeline.

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

[**D3D12 \_ \_ DESC DE SAÍDA \_ DE FLUXO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)
</dt> </dl>

 

 





