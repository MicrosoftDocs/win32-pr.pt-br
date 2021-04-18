---
title: Método ID3DX12PipelineParserCallbacks FlagsCb (D3DX12. h)
description: Chama o retorno de chamada do subobjeto flags de um objeto que implementa essa interface.
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
ms.openlocfilehash: f30ac5a0ca3a749144e263a1d993166b8e13ddac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772520"
---
# <a name="id3dx12pipelineparsercallbacksflagscb-method"></a>Método ID3DX12PipelineParserCallbacks:: FlagsCb

Chama o retorno de chamada do subobjeto flags de um objeto que implementa essa interface.

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

Tipo: **[ **\_ sinalizadores de \_ estado \_ do pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)**

Detalhes do subobjeto flags analisado de um fluxo de estado do pipeline.

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

[**\_Sinalizadores de \_ estado do pipeline D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)
</dt> </dl>

 

 





