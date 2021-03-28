---
title: Interface ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Uma interface de amostra acessa o estado de amostra.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interface ID3DX11EffectSamplerVariable Direct3D 11
- Interface ID3DX11EffectSamplerVariable Direct3D 11, descrita
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
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092001"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interface ID3DX11EffectSamplerVariable

Uma interface de amostra acessa o estado de amostra.

## <a name="members"></a>Membros

A interface **ID3DX11EffectSamplerVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectSamplerVariable** tem esses métodos.



| Método                                                                  | Descrição                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Obtenha um ponteiro para uma variável que contém o estado de amostra.<br/> |
| [**Getamostrar**](id3dx11effectsamplervariable-getsampler.md)           | Obtenha um ponteiro para uma interface de amostra.<br/>                    |
| [**Setamostrar**](id3dx11effectsamplervariable-setsampler.md)           | Defina o estado de amostra.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Reverter um estado de amostra definido anteriormente.<br/>                   |



 

## <a name="remarks"></a>Comentários

Uma interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) é criada quando um efeito é lido na memória.

As variáveis de efeito são salvas na memória no repositório de backup; Quando uma técnica é aplicada, os valores no repositório de backup são copiados para o dispositivo. Você pode usar qualquer um desses métodos para retornar o estado.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





