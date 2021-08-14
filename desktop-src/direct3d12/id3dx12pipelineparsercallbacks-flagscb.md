---
title: Método FlagsCb ID3DX12PipelineParserCallbacks (D3DX12.h)
description: Chama o retorno de chamada de subobjeto de sinalizadores de um objeto que implementa essa interface.
ms.assetid: 81DD8CF3-87BA-4380-BECD-70A80580048A
keywords:
- Método FlagsCb
- Método FlagsCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método FlagsCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.FlagsCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14e8b507ae04a5f35b2786ca4ba7ab6ec19bb449492aa2c40f32510cd3ecb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528778"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>Método ID3DX12PipelineParserCallbacks::FlagsCb

Chama o retorno de chamada de subobjeto de sinalizadores de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void FlagsCb(
   D3D12_PIPELINE_STATE_FLAGS Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* 
</dt> <dd>

Tipo: **[ **SINALIZADORES DE ESTADO DO \_ PIPELINE \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Detalhes do subobjeto de sinalizadores analisados de um fluxo de estado de pipeline.

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

[**SINALIZADORES DE ESTADO DO PIPELINE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





