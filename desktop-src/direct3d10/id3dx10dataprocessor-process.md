---
description: Processar alguns dados.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: 'ID3DX10DataProcessor: método modelos de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173213"
---
# <a name="id3dx10dataprocessorprocess-method"></a>ID3DX10DataProcessor: método modelos de:P

Processar alguns dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **void \***

Ponteiro para os dados a serem processados.

</dd> <dt>

*cBytes* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**

Tamanho dos dados a serem processados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
