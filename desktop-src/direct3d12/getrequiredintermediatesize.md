---
title: Função GetRequiredIntermediateSize (D3dx12. h)
description: Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Função GetRequiredIntermediateSize
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752179"
---
# <a name="getrequiredintermediatesize-function"></a>Função GetRequiredIntermediateSize

Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.

## <a name="syntax"></a>Sintaxe


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestinationResource* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Um ponteiro para a interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) que representa o recurso de destino.

</dd> <dt>

*FirstSubresource* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice do primeiro subrecurso no recurso. O intervalo de valores válidos é de 0 a D3D12 \_ req \_ subrecursos.

</dd> <dt>

*NumSubresources* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de subrecursos no recurso. O intervalo de valores válidos é de 0 a (D3D12 \_ req \_ subresources- *FirstSubresource*).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

O tamanho do buffer, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

