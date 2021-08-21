---
title: Método ID3DX11EffectPass GetDesc (D3dx11effect.h)
description: Obter uma descrição de aprovação.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11 , interface ID3DX11EffectPass
- ID3DX11EffectPass interface Direct3D 11 , método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd75b5b23e253715af33c712fe957ae057b681f715a60fa37d4451c3fc76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535062"
---
# <a name="id3dx11effectpassgetdesc-method"></a>Método ID3DX11EffectPass::GetDesc

Obter uma descrição de aprovação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)\***

Um ponteiro para uma descrição de passagem (consulte [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Uma passagem é um bloco de código que define o estado de renderização e sombreadores (que, por sua vez, define buffers constantes, amostras e texturas). Uma técnica de efeito contém uma ou mais passagens.

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





