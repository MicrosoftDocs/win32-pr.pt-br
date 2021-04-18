---
description: Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave armazenado em um formato de dados compactado.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interface ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105756795"
---
# <a name="id3dxcompressedanimationset-interface"></a>Interface ID3DXCompressedAnimationSet

Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave armazenado em um formato de dados compactado.

## <a name="members"></a>Membros

A interface **ID3DXCompressedAnimationSet** herda de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXCompressedAnimationSet** tem esses métodos.



| Método                                                                                  | Descrição                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetCallbackKeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.<br/>   |
| [**GetCompressedData**](id3dxcompressedanimationset--getcompresseddata.md)             | Obtém o buffer de dados que armazena dados de animação de quadro chave compactados.<br/> |
| [**GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Obtém o número de chaves de retorno de chamada no conjunto de animações.<br/>                |
| [**Getreproduzirtype**](id3dxcompressedanimationset--getplaybacktype.md)                 | Obtém o tipo do loop de reprodução do conjunto de animação.<br/>                     |
| [**GetSourceTicksPerSecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Obtém o número de tiques de quadros-chave de animação que ocorrem por segundo.<br/>   |



 

## <a name="remarks"></a>Comentários

Crie uma animação de quadro chave de formato compactado definida com [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).

O tipo LPD3DXCOMPRESSEDANIMATIONSET é definido como um ponteiro para essa interface.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
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

 

 




