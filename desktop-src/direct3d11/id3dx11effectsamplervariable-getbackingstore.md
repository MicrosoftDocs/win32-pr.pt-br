---
title: Método GetBackingStore ID3DX11EffectSamplerVariable (D3dx11effect.h)
description: Obter um ponteiro para uma variável que contém o estado do sampler.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11 , interface ID3DX11EffectSamplerVariable
- ID3DX11EffectSamplerVariable interface Direct3D 11 , método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51bba7ff1c23a7b842fc6f41ea623b19096b4cbf1691e5645d32cc1df02a2bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534162"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>Método ID3DX11EffectSamplerVariable::GetBackingStore

Obter um ponteiro para uma variável que contém o estado do sampler.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indexe em uma matriz de descrições de amostra. Se houver apenas uma variável de amostra no efeito, use 0.

</dd> <dt>

*pSamplerDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Um ponteiro para uma descrição do amostrador (consulte [**D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

