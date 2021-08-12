---
description: A interface ID3DX10Sprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D. Essa interface pode operar em um conjunto de vários sprites.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: Interface ID3DX10Sprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301924"
---
# <a name="id3dx10sprite-interface"></a>Interface ID3DX10Sprite

A interface ID3DX10Sprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D. Essa interface pode operar em um conjunto de vários sprites.

## <a name="members"></a>Membros

A interface **ID3DX10Sprite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Sprite** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10Sprite** tem esses métodos.



| Método                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Começar**](id3dx10sprite-begin.md)                                   | Prepare um dispositivo para desenhar sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Adicione uma matriz de sprites ao lote de sprites a serem renderizados. Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)e [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) deve ser chamado antes de end enviar todos os sprites em lote para o dispositivo para renderização. Esse método Draw é mais útil ao desenhar um pequeno número de sprites que você deseja armazenar em buffer em um lote grande, como fontes.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Desenhe uma matriz de sprites. Isso enviará imediatamente os sprites para o dispositivo para renderização, que é diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que adiciona apenas uma matriz de sprites a um lote de sprites a serem renderizados quando [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) é chamado. Esse método Draw é mais útil ao desenhar um grande número de sprites que já foram classificados na CPU (ou não precisam ser classificados), como em um sistema de partículas. Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md).<br/> |
| [**End**](id3dx10sprite-end.md)                                       | Chame isso após ID3DX10Sprite:: flush. Se \_ o estado de salvamento de Sprite do D3DX10 \_ \_ tiver sido especificado quando ID3DX10Sprite:: BEGIN for chamado, essa API restaurará o estado do dispositivo para como ele estava antes de ID3DX10Sprite:: Begin ser chamado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Liberar**](id3dx10sprite-flush.md)                                   | Forçar a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite:: Begin. A lista de sprites em lote é desmarcada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Recupere o dispositivo associado ao objeto Sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Obtenha a matriz de projeção Sprite que é aplicada a todos os sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Obter a transformação de exibição que se aplica a todos os sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Defina a matriz de projeção para todos os sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Defina a transformação da exibição que se aplica a todos os sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

A interface ID3DX10Sprite é obtida chamando a função [**D3DX10CreateSprite**](d3dx10createsprite.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
