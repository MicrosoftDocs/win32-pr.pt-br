---
description: Retorna o índice de amostra.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: Método ID3DXConstantTable::GetSamplerIndex (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dac22cc15e93198e7d494986b2279ae7e1d11fdb3c8cb65b3caddf9b905595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987566"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>Método ID3DXConstantTable::GetSamplerIndex

Retorna o índice de amostra.

## <a name="syntax"></a>Sintaxe


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ out\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

O alça do sampler.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Retorna o número do índice de amostra da tabela constante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
