---
description: Usado para descompactar dados codificados. Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader: método ecompress de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781144"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader: método ecompress de:D

Usado para descompactar dados codificados. Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppData* \[ fora\]
</dt> <dd>

Tipo: **void \* \***

Ponteiro para os dados brutos a serem descompactados.

</dd> <dt>

*pcBytes* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

O tamanho dos dados apontados por ppData.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

A [**interface ID3DX10DataLoader**](id3dx10dataloader.md) pode ser herdada e seus membros redefinidos. A descompactação pode ser redefinida para dar suporte aos seus próprios formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
