---
title: Método decompactar ID3DX11DataLoader (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Descompacta dados codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Método de descompactação do Direct3D 11
- Método descompactar o Direct3D 11, interface ID3DX11DataLoader
- Interface ID3DX11DataLoader Direct3D 11, método decompactar
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930752"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader: método ecompress de:D

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Descompacta dados codificados.

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

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)\***

O tamanho dos dados apontados por ppData.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Use esse método para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.

A [**interface ID3DX11DataLoader**](id3dx11dataloader.md) pode ser herdada e seus membros redefinidos para dar suporte a formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

