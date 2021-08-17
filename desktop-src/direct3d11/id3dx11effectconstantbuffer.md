---
title: Interface ID3DX11EffectConstantBuffer (D3dx11effect.h)
description: Uma interface de buffer constante acessa buffers constantes ou buffers de textura.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- ID3DX11EffectConstantBuffer interface Direct3D 11
- ID3DX11EffectConstantBuffer interface Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c5e62e6d339482123f66b7f23aae771f335392b54b9a766681dab78f6fbafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851636"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Interface ID3DX11EffectConstantBuffer

Uma interface de buffer constante acessa buffers constantes ou buffers de textura.

## <a name="members"></a>Membros

A interface **ID3DX11EffectConstantBuffer** herda [**de ID3DX11EffectVariable.**](id3dx11effectvariable.md) **ID3DX11EffectConstantBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectConstantBuffer** tem esses métodos.



| Método                                                                             | Descrição                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Obter um buffer constante.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Obter um buffer de textura.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Definir um buffer constante.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Definir um buffer de textura.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Reverte um buffer constante definido anteriormente.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Reverte um buffer de textura definido anteriormente.<br/>  |



 

## <a name="remarks"></a>Comentários

Use buffers constantes para armazenar muitas constantes de efeito; agrupando constantes em buffers com base na frequência de atualização. Isso permite minimizar o número de alterações de estado, bem como fazer o menor número de chamadas à API para alterar o estado. Esses dois fatores levam a um melhor desempenho.

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

 

 





