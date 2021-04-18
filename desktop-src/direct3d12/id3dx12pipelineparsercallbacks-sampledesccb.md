---
title: Método ID3DX12PipelineParserCallbacks SampleDescCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto de descrição de exemplo de um objeto que implementa essa interface.
ms.assetid: 32F112D3-97B1-45C2-8744-9F27DC95C249
keywords:
- Método SampleDescCb
- Método SampleDescCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método SampleDescCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleDescCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0644837720dd8c81dc1c7577a1d6506ebdf61c24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802103"
---
# <a name="id3dx12pipelineparsercallbackssampledesccb-method"></a>Método ID3DX12PipelineParserCallbacks:: SampleDescCb

Chama o retorno de chamada de subobjeto de descrição de exemplo de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void SampleDescCb(
  [ref] const DXGI_SAMPLE_DESC &SampleDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SampleDesc* \[ referência\]
</dt> <dd>

Tipo: **const [**dxgi \_ amostra \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)**

Detalhes do subobjeto de descrição de exemplo analisado a partir de um fluxo de estado de pipeline.

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

[**\_desc de exemplo de dxgi \_**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)
</dt> </dl>

 

