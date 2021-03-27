---
title: Método de processo ID3DX11DataProcessor (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Processa dados.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Método de processo Direct3D 11
- Método de processo Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, método de processo
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506493"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor: método modelos de:P

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Processa dados.

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

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamanho dos dados a serem processados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Esse método é usado por uma [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

