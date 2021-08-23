---
description: Crie um recurso de textura de um arquivo que reside na memória do sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Função D3DX10CreateTextureFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7b64c3c429ef356fa4ab8c206682c3b1711a14fe29ee6b2024b92b8113951062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753346"
---
# <a name="d3dx10createtexturefrommemory-function"></a>Função D3DX10CreateTextureFromMemory

Crie um recurso de textura de um arquivo que reside na memória do sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para o dispositivo (consulte [**Interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que usará o recurso.

</dd> <dt>

*pSrcData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o recurso na memória do sistema.

</dd> <dt>

*SrcDataSize* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Tamanho do recurso na memória do sistema.

</dd> <dt>

*pLoadInfo* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) quando o processador de dados é criado; de definido como **NULL** para ler as características de uma textura quando a textura é carregada.

</dd> <dt>

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Um ponteiro para uma interface de bomba de thread (consulte Interface [**ID3DX10ThreadPump**](id3dx10threadpump.md)). Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***

Endereço de um ponteiro para o recurso criado. Consulte [**Interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL.** Se *pPump* não for **NULL,** *o pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Para ver uma lista dos formatos de imagem com suporte, consulte FORMATO DE ARQUIVO DE IMAGEM [**D3DX10 \_ \_ \_**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
