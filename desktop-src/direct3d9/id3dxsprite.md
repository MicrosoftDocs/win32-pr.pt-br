---
description: A interface ID3DXSprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interface ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837947"
---
# <a name="id3dxsprite-interface"></a>Interface ID3DXSprite

A interface ID3DXSprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.

## <a name="members"></a>Membros

A interface **ID3DXSprite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSprite** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXSprite** tem esses métodos.



| Método                                                | Descrição                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Começar**](id3dxsprite--begin.md)                   | Prepara um dispositivo para desenhar sprites.<br/>                                                                                                                                                                            |
| [**Draw**](id3dxsprite--draw.md)                     | Adiciona um Sprite à lista de sprites em lote.<br/>                                                                                                                                                                     |
| [**Completo**](id3dxsprite--end.md)                       | Chama [**ID3DXSprite:: flush**](id3dxsprite--flush.md) e restaura o estado do dispositivo para como ele estava antes de [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) foi chamado.<br/>                                            |
| [**Liberar**](id3dxsprite--flush.md)                   | Força a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). A lista de sprites em lote é desmarcada.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Recupera o dispositivo associado ao objeto Sprite.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Obtém a transformação de Sprite.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Use este método para readquirir recursos e salvar o estado inicial.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Define a transformação Sprite.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Define a transformação de exibição Mundial da mão esquerda para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Define a transformação de exibição Mundial da mão direita para um Sprite. Uma chamada para esse método é necessária antes de obter ou classificar sprites.<br/>                                                                                |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXSprite** é obtida chamando a função [**D3DXCreateSprite**](d3dxcreatesprite.md) .

Normalmente, o aplicativo primeiro chama [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), que permite o controle sobre o estado de renderização do dispositivo, a mistura alfa e a transformação e classificação de Sprite. Em seguida, para cada sprite a ser exibido, chame [**ID3DXSprite::D RAW**](id3dxsprite--draw.md). **ID3DXSprite::D RAW** pode ser chamado repetidamente para armazenar qualquer número de sprites. Para exibir os sprites em lote para o dispositivo, chame [**ID3DXSprite:: End**](id3dxsprite--end.md) ou [**ID3DXSprite:: flush**](id3dxsprite--flush.md).

O tipo LPD3DXSPRITE é definido como um ponteiro para a interface **ID3DXSprite** .


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
