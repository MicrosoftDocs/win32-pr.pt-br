---
title: Interface ID3DX11EffectSamplerVariable (D3dx11effect.h)
description: Uma interface de amostra acessa o estado do amostrador.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- ID3DX11EffectSamplerVariable interface Direct3D 11
- ID3DX11EffectSamplerVariable interface Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0865df924fb3a01e3c10ae015f13b4ec6e06e900dad32ff966d9bdbfed0c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952816"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interface ID3DX11EffectSamplerVariable

Uma interface de amostra acessa o estado do amostrador.

## <a name="members"></a>Membros

A interface **ID3DX11EffectSamplerVariable herda** de [**ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectSamplerVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectSamplerVariable** tem esses métodos.



| Método                                                                  | Descrição                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Obter um ponteiro para uma variável que contém o estado do sampler.<br/> |
| [**GetSampler**](id3dx11effectsamplervariable-getsampler.md)           | Obter um ponteiro para uma interface de amostra.<br/>                    |
| [**SetSampler**](id3dx11effectsamplervariable-setsampler.md)           | Definir o estado do sampler.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Reverter um estado de amostra definido anteriormente.<br/>                   |



 

## <a name="remarks"></a>Comentários

Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.

As variáveis de efeito são salvas na memória no armazenamento de back-back; quando uma técnica é aplicada, os valores no armazenamento de back-back são copiados para o dispositivo. Você pode usar qualquer um desses métodos para retornar o estado.

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 Interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





