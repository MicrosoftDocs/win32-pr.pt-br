---
title: Método Descompactador ID3DX11DataLoader (D3DX11core.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Descompacta dados codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Método Descompactar Direct3D 11
- Método Descompactar Direct3D 11 , interface ID3DX11DataLoader
- ID3DX11DataLoader interface Direct3D 11 , método Descompactar
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
ms.openlocfilehash: 8a4f2424d46748b33918c8b6870c07dbaf4486217f8f3ba7a0a64f881792b81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633026"
---
# <a name="id3dx11dataloaderdecompress-method"></a>Método ID3DX11DataLoader::D ecompress

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

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

*ppData* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Ponteiro para os dados brutos a descompactar.

</dd> <dt>

*pcBytes* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)\***

O tamanho dos dados apontados por ppData.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Use esse método para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.

[**A Interface ID3DX11DataLoader**](id3dx11dataloader.md) pode ser herdada e seus membros redefinidos para dar suporte a formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

