---
title: Método HSCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chama o retorno de chamada do subobjeto do sombreador de chassi de um objeto que implementa essa interface.
ms.assetid: B2967E7F-391F-4A76-A087-E0B925018EE3
keywords:
- Método HSCb
- Método HSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método HSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.HSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abac62d531f995d223fc970b9a228fc653e26f52992f22b52fbea2a69757d276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807271"
---
# <a name="id3dx12pipelineparsercallbackshscb-method"></a>Método ID3DX12PipelineParserCallbacks::HSCb

Chama o retorno de chamada do subobjeto do sombreador de chassi de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void HSCb(
  [ref] const D3D12_SHADER_BYTECODE &HS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HS* \[ Ref\]
</dt> <dd>

Tipo: **const [**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalhes do subobjeto do sombreador de chassi analisado de um fluxo de estado do pipeline.

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

[**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





