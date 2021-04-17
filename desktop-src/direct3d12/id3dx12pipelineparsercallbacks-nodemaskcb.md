---
title: Método ID3DX12PipelineParserCallbacks NodemaskCb (D3DX12. h)
description: Chama o retorno de chamada de subobjeto nodemask de um objeto que implementa essa interface.
ms.assetid: F5A408B7-A777-4BBC-A2A3-1BC3551E65ED
keywords:
- Método NodemaskCb
- Método NodemaskCb, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método NodemaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.NodemaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf1cc03f60259c395ca8c459ddd5a308e3dcd6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812089"
---
# <a name="id3dx12pipelineparsercallbacksnodemaskcb-method"></a>Método ID3DX12PipelineParserCallbacks:: NodemaskCb

Chama o retorno de chamada de subobjeto nodemask de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void NodemaskCb(
   
        UINT
       Nodemask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nodemask* 
</dt> <dd>

Tipo: **uint**

Detalhes do subobjeto nodemask analisado de um fluxo de estado do pipeline.

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
</dt> </dl>

 

 





