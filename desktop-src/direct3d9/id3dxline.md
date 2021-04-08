---
description: A interface ID3DXLine implementa o desenho de linha usando triângulos texturizados.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interface ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012186"
---
# <a name="id3dxline-interface"></a>Interface ID3DXLine

A interface ID3DXLine implementa o desenho de linha usando triângulos texturizados.

## <a name="members"></a>Membros

A interface **ID3DXLine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXLine** tem esses métodos.



| Método                                                | Descrição                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Começar**](id3dxline--begin.md)                     | Prepara um dispositivo para linhas de desenho.<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | Desenha uma faixa de linha no espaço da tela. A entrada está na forma de uma matriz que define pontos (de [**D3DXVECTOR2**](d3dxvector2.md)) na faixa de linha.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.<br/>                                                                                                      |
| [**Completo**](id3dxline--end.md)                         | Restaura o estado do dispositivo para como ele era quando [**ID3DXLine:: Begin**](id3dxline--begin.md) foi chamado.<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Obtém o estado de anti-aliasing da linha.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera o dispositivo Direct3D associado ao objeto line.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Obtém o modo de desenho de linha no estilo OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Obtém o padrão de Stipple de linha.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Obtém o valor de escala Stipple-Pattern.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Obtém a espessura da linha.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Use este método para readquirir recursos e salvar o estado inicial.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Alterna a suavização de linha.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Alterna o modo para desenhar linhas no estilo OpenGL.<br/>                                                                                                                                          |
| [**Setpattern**](id3dxline--setpattern.md)           | Aplica um padrão Stipple à linha.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Amplia o padrão Stipple ao longo da direção da linha.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Especifica a espessura da linha.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Comentários

Crie um objeto de desenho de linha com [**D3DXCreateLine**](d3dxcreateline.md).

O tipo LPD3DXLINE é definido como um ponteiro para a interface **ID3DXLine** .


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
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

 

 
