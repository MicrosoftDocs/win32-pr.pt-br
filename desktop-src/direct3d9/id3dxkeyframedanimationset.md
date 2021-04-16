---
description: Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interface ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789616"
---
# <a name="id3dxkeyframedanimationset-interface"></a>Interface ID3DXKeyframedAnimationSet

Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave.

## <a name="members"></a>Membros

A interface **ID3DXKeyframedAnimationSet** herda de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXKeyframedAnimationSet** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compactar**](id3dxkeyframedanimationset--compress.md)                                 | Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.<br/> |
| [**GetCallbackKey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Obtém informações sobre um retorno de chamada específico no conjunto de animações.<br/>                                                                        |
| [**GetCallbackKeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.<br/>                                                                     |
| [**GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Obtém o número de chaves de retorno de chamada no conjunto de animações.<br/>                                                                                  |
| [**GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Obtém o número de chaves de rotação na animação do quadro chave especificado.<br/>                                                                  |
| [**GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Obtém o número de chaves de escala na animação do quadro chave especificado.<br/>                                                                     |
| [**GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Obtém o número de chaves de tradução na animação do quadro chave especificado.<br/>                                                               |
| [**Getreproduzirtype**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Obtém o tipo do loop de reprodução do conjunto de animação.<br/>                                                                                       |
| [**GetRotationKey**](id3dxkeyframedanimationset--getrotationkey.md)                     | Obter informações de rotação para um quadro-chave específico no conjunto de animações.<br/>                                                                 |
| [**GetRotationKeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.<br/>                                                                   |
| [**GetScaleKey**](id3dxkeyframedanimationset--getscalekey.md)                           | Obter informações de escala para um quadro-chave específico no conjunto de animações.<br/>                                                                    |
| [**GetScaleKeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | Preenche uma matriz com dados de chave de escala usados para animação de quadro chave.<br/>                                                                        |
| [**GetSourceTicksPerSecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Obtém o número de tiques de quadros-chave de animação que ocorrem por segundo.<br/>                                                                     |
| [**GetTranslationKey**](id3dxkeyframedanimationset--gettranslationkey.md)               | Obter informações de tradução para um quadro-chave específico no conjunto de animações.<br/>                                                              |
| [**GetTranslationKeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Preenche uma matriz com dados de chave de tradução usados para animação de quadro chave.<br/>                                                                |
| [**RegisterAnimationSRTKeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.<br/>                                                        |
| [**SetCallbackKey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Define informações sobre um retorno de chamada específico no conjunto de animações.<br/>                                                                        |
| [**SetRotationKey**](id3dxkeyframedanimationset--setrotationkey.md)                     | Defina informações de rotação para um quadro-chave específico no conjunto de animações.<br/>                                                                 |
| [**SetScaleKey**](id3dxkeyframedanimationset--setscalekey.md)                           | Defina informações de escala para um quadro-chave específico no conjunto de animações.<br/>                                                                    |
| [**SetTranslationKey**](id3dxkeyframedanimationset--settranslationkey.md)               | Definir informações de tradução para um quadro-chave específico no conjunto de animações.<br/>                                                              |
| [**UnregisterAnimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | Remova os dados de animação do conjunto de animações.<br/>                                                                                       |
| [**UnregisterRotationKey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Remove os dados de rotação no quadro de chave especificado.<br/>                                                                                   |
| [**UnregisterScaleKey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Remove os dados de escala no quadro de chave especificado.<br/>                                                                                      |
| [**UnregisterTranslationKey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Remove os dados de tradução no quadro de chave especificado.<br/>                                                                                |



 

## <a name="remarks"></a>Comentários

Crie uma animação de quadro chave definida com [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

O tipo LPD3DXKEYFRAMEDANIMATIONSET é definido como um ponteiro para essa interface.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




