---
title: Função D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca matemática de harmônicas esféricas, SHProjectCubeMap.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Função D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989331"
---
# <a name="d3dx11shprojectcubemap-function"></a>Função D3DX11SHProjectCubeMap

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [matemática de harmônicas esféricas](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) , **SHProjectCubeMap**.

 

Projeta uma função representada em um mapa de cubo em harmônicas esféricas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*Ordem* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ordem da avaliação SH, gera coeficientes de ordem ^ 2 cujo grau é a ordem 1. O intervalo válido está entre 2 e 6.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Um ponteiro para um [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa um cubemap que vai ser projetado em harmônicas esféricas.

</dd> <dt>

*pROut* 
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Vetor SH de saída para vermelho.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Gerar vetor de saída para verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Vetor SH de saída para azul.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

