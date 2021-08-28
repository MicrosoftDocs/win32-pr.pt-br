---
title: Função D3DX11CreateShaderResourceViewFromMemory (D3DX11tex. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Observação em vez de usar essa função, recomendamos que você use essas DirectXTK library (Runtime), CreateXXXTextureFromMemory (em que XXX é DDS ou WIC) DirectXTex library (Tools), LoadFromXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, CreateShaderResourceView criar uma exibição de recurso de sombreador de um arquivo na memória.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- Função D3DX11CreateShaderResourceViewFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d242885fc09ee513f5107298f1bac98b5cb9cb684de0f6e85e960fb9c7078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124731"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a>Função D3DX11CreateShaderResourceViewFromMemory

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você as use:
>
> -   [DirectXTK](https://github.com/Microsoft/DirectXTK) library (Runtime), **CreateXXXTextureFromMemory** (em que xxx é DDS ou WIC)
> -   Biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), **LoadFromXXXMemory** (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, **CreateShaderResourceView**

 

Criar um sombreador – modo de exibição de recursos de um arquivo na memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Um ponteiro para o dispositivo (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará o recurso.

</dd> <dt>

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Ponteiro para o arquivo na memória que contém a exibição do sombreador-recurso.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamanho do arquivo na memória.

</dd> <dt>

*pLoadInfo* \[ no\]
</dt> <dd>

Tipo: **[ **\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**\_ informações de \_ carregamento \_ de imagem D3DX11**](d3dx11-image-load-info.md)) quando o processador de dados é criado; defina isso como **nulo** para ler as características de uma textura quando a textura for carregada.

</dd> <dt>

*pPump* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)). Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.

</dd> <dt>

*ppShaderResourceView* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Endereço de um ponteiro para o modo de exibição de recursos do sombreador recém-criado. Consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).

</dd> <dt>

*pHResult* \[ fora\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL**. Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

