---
title: Função D3DX11CreateAsyncShaderPreprocessProcessor (D3DX11async.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um processador de dados para um sombreador de forma assíncrona.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- Função D3DX11CreateAsyncShaderPreprocessProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e19d0e4d8c2f722e1de882cb265ec6df4e206c5d845f535643c07feb672a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124881"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a>Função D3DX11CreateAsyncShaderPreprocessProcessor

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.

 

Crie um processador de dados para um sombreador de forma assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Uma cadeia de caracteres que contém o nome do arquivo do sombreador.

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const D3D11 \_ SHADER \_ MACRO \***

Uma matriz terminada em NULL de macros de sombreador; de definir isso como **NULL** para especificar nenhuma macro.

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Um ponteiro para uma interface de inclusão; de definido como **NULL** para especificar que não há nenhum arquivo de inclusão.

</dd> <dt>

*ppShaderText* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para um buffer que contém o texto ASCII do sombreador.

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***

Endereço de um ponteiro para um buffer que contém erros de compilação.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte Interface [**ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e do D3DX 11.

Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o exemplo de tutorial do [Direct3D)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

Para aplicativos da área de trabalho Win32, você pode usar o [Runtime de Simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação assíncrona Windows Runtime.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11async.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

