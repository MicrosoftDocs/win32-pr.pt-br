---
description: Crie um efeito da memória.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: Função D3DX10CreateEffectFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 3bcc32e94d6329d42edd27f1daf39e40d28b71ba65cc32fd88d4ae3951d5012e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989236"
---
# <a name="d3dx10createeffectfrommemory-function"></a>Função D3DX10CreateEffectFromMemory

Crie um efeito da memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o efeito na memória.

</dd> <dt>

*DataLength* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamanho do efeito na memória.

</dd> <dt>

*pSrcFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do arquivo de efeito na memória.

</dd> <dt>

*pDefines* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Uma matriz terminada em NULL de macros de sombreador (consulte  MACRO DO [**\_ SOMBREADOR \_ D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); de definido como NULL para não especificar macros.

</dd> <dt>

*pInclude* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Um ponteiro para uma interface de inclusão (consulte [**Interface ID3D10Incluir**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))). Este parâmetro pode ser **NULL**.

</dd> <dt>

*pProfile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que especifica o [perfil do sombreador](../direct3dhlsl/dx-graphics-hlsl-models.md)ou o modelo de sombreador.

</dd> <dt>

*HLSLFlags* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opções de compilação HLSL (consulte [Constantes de \_ SOMBREADOR D3D10](d3d10-shader.md)).

</dd> <dt>

*FXFlags* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opções de compilação de efeito (consulte [ \_ Constantes D3D10 EFFECT](d3d10-effect.md)).

</dd> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para o dispositivo (consulte [**Interface ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) que usará os recursos.

</dd> <dt>

*pEffectPool* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***

Ponteiro para um pool de efeitos (consulte [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) para compartilhar variáveis entre efeitos.

</dd> <dt>

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bomba de thread (consulte Interface [**ID3DX10ThreadPump**](id3dx10threadpump.md)). Use **NULL** para especificar que essa função não deve retornar até que seja concluída.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***

Endereço de um ponteiro para o efeito (consulte [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) que é criado.

</dd> <dt>

*ppErrors* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

O endereço de um ponteiro para a memória (consulte [**Interface ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contém erros de compilação de efeito, se houver algum.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL.** Se *pPump* não for **NULL,** *o pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
