---
description: Cria uma malha que contém o texto especificado, usando a fonte associada ao contexto do dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Função D3DXCreateText (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9db7cc6fa89f8f102cabccdebd14852a50f60576b6135ae52e4cc9fada494812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732290"
---
# <a name="d3dxcreatetext-function"></a>Função D3DXCreateText

Cria uma malha que contém o texto especificado, usando a fonte associada ao contexto do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para o dispositivo que criou a malha.

</dd> <dt>

*hDC* \[ Em\]
</dt> <dd>

Tipo: **HDC**

Contexto do dispositivo, que contém a fonte para saída. A fonte selecionada pelo contexto do dispositivo deve ser uma fonte TrueType.

</dd> <dt>

*pText* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o texto a ser gerado. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*Desvio* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Desvio máximo de acordo com as estruturas de fonte TrueType.

</dd> <dt>

*Ltdion* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor para extrudir texto na direção z negativa.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para a malha retornada.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para um buffer que contém informações de adjacency. Pode ser **NULL.**

</dd> <dt>

*pGlyphMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Ponteiro para uma matriz de [**estruturas GLIPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) que contêm os dados de métrica de glifo. Cada elemento contém informações sobre a posição e a orientação do glifo correspondente na cadeia de caracteres. O número de elementos na matriz deve ser igual ao número de caracteres na cadeia de caracteres. Observe que a origem em cada estrutura não é relativa à cadeia de caracteres inteira, mas é relativa a essa célula de caractere. Para calcular toda a caixa delimitada, adicione o incremento para cada glifo ao percorrer a cadeia de caracteres. Se você não estiver preocupado com os tamanhos de glifo, de definir esse parâmetro como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXCreateTextW. Caso contrário, a chamada de função será resolvida para D3DXCreateTextA porque as cadeias de caracteres ANSI estão sendo usadas.

Essa função cria uma malha com a opção de criação GERENCIADA D3DXMESH e o formato de vértice flexível \_ [ \_ \| D3DFVF XYZ D3DFVF \_ NORMAL](d3dfvf.md) (FVF).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de desenho de forma](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
