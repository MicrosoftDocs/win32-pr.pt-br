---
description: A interface ID3DXLine implementa o desenho de linha usando triângulos com textura.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interface ID3DXLine (D3dx9core.h)
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
ms.openlocfilehash: a9677ca802a800624b374212c6942ab6676423f8d63e62cbf136a8b9e69c533d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951366"
---
# <a name="id3dxline-interface"></a>Interface ID3DXLine

A interface ID3DXLine implementa o desenho de linha usando triângulos com textura.

## <a name="members"></a>Membros

A interface **ID3DXLine** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLine** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXLine** tem esses métodos.



| Método                                                | Descrição                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Começar**](id3dxline--begin.md)                     | Prepara um dispositivo para desenhar linhas.<br/>                                                                                                                                                  |
| [**Draw**](id3dxline--draw.md)                       | Desenha uma faixa de linha no espaço da tela. A entrada está na forma de uma matriz que define pontos [**(de D3DXVECTOR2**](d3dxvector2.md)) na faixa de linha.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.<br/>                                                                                                      |
| [**End**](id3dxline--end.md)                         | Restaura o estado do dispositivo como estava quando [**ID3DXLine::Begin**](id3dxline--begin.md) foi chamado.<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Obtém o estado de aninhamento de linha.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera o dispositivo Direct3D associado ao objeto de linha.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Obtém o modo de desenho de linha no estilo OpenGL.<br/>                                                                                                                                              |
| [**Getpattern**](id3dxline--getpattern.md)           | Obtém o padrão de apple de linha.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Obtém o valor de escala padrão da apple.<br/>                                                                                                                                                 |
| [**Getwidth**](id3dxline--getwidth.md)               | Obtém a espessura da linha.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Use esse método para adquirir recursos e salvar o estado inicial.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Alterna a antialiação de linha.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Alterna o modo para desenhar linhas no estilo OpenGL.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Aplica um padrão de replicação à linha.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Alonga o padrão de apple ao longo da direção da linha.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Especifica a espessura da linha.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Comentários

Crie um objeto de desenho de linha [**com D3DXCreateLine**](d3dxcreateline.md).

O tipo LPD3DXLINE é definido como um ponteiro para a interface **ID3DXLine.**


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
