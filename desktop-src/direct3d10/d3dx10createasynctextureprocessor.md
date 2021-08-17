---
description: Função D3DX10CreateAsyncTextureProcessor – crie um processador de dados a ser usado com uma bomba de thread.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Função D3DX10CreateAsyncTextureProcessor (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d245a96181e194479b0c5e115b3b3aea89096da8176713047578a93264e470da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852356"
---
# <a name="d3dx10createasynctextureprocessor-function"></a>Função D3DX10CreateAsyncTextureProcessor

Crie um processador de dados a ser usado com uma [**bomba de thread**](id3dx10threadpump.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para a desaqueia (consulte [**Interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).

</dd> <dt>

*pLoadInfo* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) quando o processador de dados é criado; de definido como **NULL** para ler as características de uma textura quando a textura é carregada.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Endereço de um ponteiro para um buffer que contém o processador de dados criado (consulte Interface [**ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Essa API cria uma interface de processador de dados e carrega a textura; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) cria a interface do processador de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




