---
title: Interface ID3DX11EffectType (D3dx11effect. h)
description: A interface ID3DX11EffectType acessa variáveis de efeito por tipo. O tempo de vida de um objeto ID3DX11EffectType é igual ao tempo de vida de seu objeto ID3DX11Effect pai.
ms.assetid: 700076ee-a5fe-4af2-a5f4-053c05d8ddf0
keywords:
- Interface ID3DX11EffectType Direct3D 11
- Interface ID3DX11EffectType Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c210ca60abc9e55b8864a2b121cf92be369a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663983"
---
# <a name="id3dx11effecttype-interface"></a>Interface ID3DX11EffectType

A interface **ID3DX11EffectType** acessa variáveis de efeito por tipo.

O tempo de vida de um objeto **ID3DX11EffectType** é igual ao tempo de vida de seu objeto [**ID3DX11Effect**](id3dx11effect.md) pai.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectType** tem esses métodos.



| Método                                                                       | Descrição                                       |
|:-----------------------------------------------------------------------------|:--------------------------------------------------|
| [**GetDesc**](id3dx11effecttype-getdesc.md)                                 | Obter uma descrição do tipo de efeito.<br/>        |
| [**GetMemberName**](id3dx11effecttype-getmembername.md)                     | Obter o nome de um membro.<br/>              |
| [**GetMemberSemantic**](id3dx11effecttype-getmembersemantic.md)             | Obter a semântica anexada a um membro.<br/> |
| [**GetMemberTypeByIndex**](id3dx11effecttype-getmembertypebyindex.md)       | Obter um tipo de membro por índice.<br/>            |
| [**GetMemberTypeByName**](id3dx11effecttype-getmembertypebyname.md)         | Obter um tipo de membro por nome.<br/>            |
| [**GetMemberTypeBySemantic**](id3dx11effecttype-getmembertypebysemantic.md) | Obter um tipo de membro por semântica.<br/>         |
| [**IsValid**](id3dx11effecttype-isvalid.md)                                 | Testa se o tipo de efeito é válido.<br/>   |



 

## <a name="remarks"></a>Comentários

Para obter informações sobre um tipo de efeito de uma variável de efeito, chame [**ID3DX11EffectVariable:: GetType**](id3dx11effectvariable-gettype.md).

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

 

 





