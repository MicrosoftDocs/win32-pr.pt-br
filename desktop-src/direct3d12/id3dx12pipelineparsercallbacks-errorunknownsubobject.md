---
title: Método ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Chama o retorno de chamada de erro de subobjeto desconhecido de um objeto que implementa essa interface.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Método ErrorUnknownSubobject
- Método ErrorUnknownSubobject, interface ID3DX12PipelineParserCallbacks
- Interface ID3DX12PipelineParserCallbacks, método ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7129969cb87bdf12a4c5eb60428aad755fa99b81cd2a6944a35f51f387af4ceb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807503"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>Método ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject

Chama o retorno de chamada de erro de subobjeto desconhecido de um objeto que implementa essa interface.

## <a name="syntax"></a>Sintaxe


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Não knownTypevalue* 
</dt> <dd>

Tipo: **uint**

O tipo de subobjeto não reconhecido do subobjeto tentado.

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
</dt> </dl>

 

 





