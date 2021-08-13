---
title: Interface ID3DX11EffectGroup (D3dx11effect. h)
description: A interface ID3DX11EffectGroup acessa um grupo de efeitos. O tempo de vida de um objeto ID3DX11EffectGroup é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interface ID3DX11EffectGroup Direct3D 11
- Interface ID3DX11EffectGroup Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa42a884be0abd15f0d16403a95d859d89cd472fc630b51ffe586e703e1a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046224"
---
# <a name="id3dx11effectgroup-interface"></a>Interface ID3DX11EffectGroup

A interface **ID3DX11EffectGroup** acessa um grupo de efeitos.

O tempo de vida de um objeto **ID3DX11EffectGroup** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectGroup** tem esses métodos.



| Método                                                                  | Descrição                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Obter uma anotação por índice.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Obter uma anotação por nome.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Obtém uma descrição do grupo.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Obtenha uma técnica por índice.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Obtenha uma técnica por nome.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Teste um efeito para ver se ele contém uma sintaxe válida.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter uma interface **ID3DX11EffectGroup** , chame um método como [**ID3DX11Effect:: getgroupbyname**](id3dx11effect-getgroupbyname.md).

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





