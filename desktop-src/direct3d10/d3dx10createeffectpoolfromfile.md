---
description: Crie um pool de efeitos a partir de um arquivo de efeito.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Função D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 500e0a72bc239b6c3f67011ed7abc0421f11cd8b9e4f67cbc86087e45027522d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753396"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a>Função D3DX10CreateEffectPoolFromFile

Crie um pool de efeitos a partir de um arquivo de efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

O nome do arquivo de efeito. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*pDefines* \[ no\]
</dt> <dd>

Tipo: **\* [**macro const \_ D3D \_ Shader**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)**

Uma matriz de macros de sombreador terminada em nulo (consulte a [**\_ \_ macro do sombreador do D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); Defina como **NULL** para não especificar nenhuma macro.

</dd> <dt>

*pInclude* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Um ponteiro para uma interface de inclusão (consulte a [**interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Este parâmetro pode ser **NULL**.

</dd> <dt>

*pProfile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo do sombreador.

</dd> <dt>

*HLSLFlags* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

HLSL opções de compilação (consulte as [ \_ constantes do sombreador d3d10](d3d10-shader.md)).

</dd> <dt>

*FXFlags* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opções de compilação de efeito (consulte [sinalizadores de compilação e efeito](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.

</dd> <dt>

*pPump* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bombeamento de thread (consulte a [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppEffectPool* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***

O endereço de um ponteiro para o pool de efeitos (consulte a [**interface ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).

</dd> <dt>

*ppErrors* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

O endereço de um ponteiro para a memória (consulte a [**interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.

</dd> <dt>

*pHResult* \[ fora\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL**. Se *pPump* não for **NULL**, *pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Este exemplo cria um pool de efeitos a partir do efeito usado no [exemplo de BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
