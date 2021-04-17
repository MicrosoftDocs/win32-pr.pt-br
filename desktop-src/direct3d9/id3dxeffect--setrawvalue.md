---
description: Defina um intervalo contíguo de constantes de sombreador com uma cópia de memória.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'Método ID3DXEffect:: SetRawValue (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812201"
---
# <a name="id3dxeffectsetrawvalue-method"></a>Método ID3DXEffect:: SetRawValue

Defina um intervalo contíguo de constantes de sombreador com uma cópia de memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Manipule o valor a ser definido ou o nome do valor passado como uma cadeia de caracteres. A passagem de um identificador é mais eficiente. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **void \***

Ponteiro para um buffer que contém os dados a serem definidos. O SetRawValue verifica a memória válida, mas não faz nenhuma verificação para dados válidos.

</dd> <dt>

*OffsetInBytes* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de bytes entre o início dos dados de efeito e o início das constantes de efeito que você vai definir.

</dd> <dt>

*Bytes* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O tamanho do buffer a ser definido, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: E \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

O SetRawValue é uma maneira muito rápida de definir constantes de efeito, pois ele executa uma cópia de memória sem executar a validação ou qualquer conversão de dados (como converter uma matriz de linha principal em uma matriz de coluna principal). Use SetRawValue para definir uma série de constantes de efeito contíguos. Por exemplo, você pode definir uma matriz de vinte matrizes com 20 chamadas para [**ID3DXBaseEffect:: setmatrix**](id3dxbaseeffect--setmatrix.md) ou usando um único SetRawValue.

Todos os valores devem ser matrix4x4s ou float4s e todas as matrizes devem estar na ordem de coluna principal. Valores int ou float são convertidos em um FLOAT4; Portanto, é altamente recomendável que você use SetRawValue com apenas dados FLOAT4 ou matrix4x4.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
