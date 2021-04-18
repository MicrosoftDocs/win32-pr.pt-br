---
title: Método ID3DX12PipelineParserCallbacks CSCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto do sombreador de computação de um objeto que implementa essa interface.
ms.assetid: DE1ABA3D-D372-4D7F-9DB6-4E3360EAFAC2
keywords:
- Método CSCb
- Método CSCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método CSCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.CSCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27dcf175d153211e06864cb73139b03f868d15db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813728"
---
# <a name="id3dx12pipelineparsercallbackscscb-method"></a>Método ID3DX12PipelineParserCallbacks:: CSCb

Chama o retorno de chamada de subobjeto do sombreador de computação de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void CSCb(
  [ref] const D3D12_SHADER_BYTECODE &CS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cs* \[ referência\]
</dt> <dd>

Tipo: **[**código de \_ \_ bytes do sombreador const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)**

Detalhes do subobjeto do sombreador de computação analisado a partir de um fluxo de estado do pipeline.

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

[**\_Código de bytes do sombreador D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> </dl>

 

 





