---
title: Método ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Obtenha um ponteiro para uma variável que contém o estado rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80912da541d5d5386da4e9612216db3ce62904bdb32ba262b5a2d1ae773201cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534682"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a>Método ID3DX11EffectRasterizerVariable:: GetBackingStore

Obtenha um ponteiro para uma variável que contém o estado rasteriser.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexe em uma matriz de descrições de rasteriser. Se houver apenas uma variável rasteriser no efeito, use 0.

</dd> <dt>

*pRasterizerDesc* 
</dt> <dd>

Tipo: **[ **D3D11 do \_ rasterizador \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***

Um ponteiro para uma descrição de rasteriser (consulte [**D3D11 \_ rasterizador \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo. O backup de dados do repositório pode ser usado para recriar a variável quando necessário.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

