---
description: Essa é uma interface implementada pelo usuário que permite que um usuário defina o estado do dispositivo de um efeito.
ms.assetid: ccd3e456-e27b-4128-b20b-99ff8dafcbe1
title: Interface ID3DXEffectStateManager (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fad9df739634625800c0a21fd9ba2a2823d70f8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298695"
---
# <a name="id3dxeffectstatemanager-interface"></a>Interface ID3DXEffectStateManager

Essa é uma interface implementada pelo usuário que permite que um usuário defina o estado do dispositivo de um efeito. Cada um dos métodos nesta interface deve ser implementado pelo usuário e, em seguida, será usado como retornos de chamada para o aplicativo quando ocorrer uma das seguintes ações:

-   Um efeito chama [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   O estado do efeito é atualizado dinamicamente chamando a API de alteração de estado apropriada. Consulte páginas de método individual para obter detalhes.

Quando um aplicativo usa o Gerenciador de estado para implementar retornos de chamada personalizados, um efeito não salva e restaura automaticamente o estado ao chamar [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md). Como o aplicativo implementou um comportamento personalizado de salvar e restaurar nos retornos de chamada, esse comportamento automático é ignorado.

## <a name="members"></a>Membros

A interface **ID3DXEffectStateManager** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXEffectStateManager** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXEffectStateManager** tem esses métodos.



| Método                                                                                | Descrição                                                                                                                  |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Clarear**](id3dxeffectstatemanager--lightenable.md)                           | Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.<br/>                                 |
| [**SetFVF**](id3dxeffectstatemanager--setfvf.md)                                     | Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.<br/>                                         |
| [**SetLight**](id3dxeffectstatemanager--setlight.md)                                 | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.<br/>                                            |
| [**SetMaterial**](id3dxeffectstatemanager--setmaterial.md)                           | Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.<br/>                                     |
| [**SetNPatchMode**](id3dxeffectstatemanager--setnpatchmode.md)                       | Uma função de retorno de chamada que deve ser implementada por um usuário para definir o número de segmentos de subdivisão para N-patches.<br/>   |
| [**SetPixelShader**](id3dxeffectstatemanager--setpixelshader.md)                     | Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de pixel.<br/>                                     |
| [**SetPixelShaderConstantB**](id3dxeffectstatemanager--setpixelshaderconstantb.md)   | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.<br/>        |
| [**SetPixelShaderConstantF**](id3dxeffectstatemanager--setpixelshaderconstantf.md)   | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante do sombreador de vértice.<br/> |
| [**SetPixelShaderConstantI**](id3dxeffectstatemanager--setpixelshaderconstanti.md)   | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.<br/>        |
| [**Setrenderingstate**](id3dxeffectstatemanager--setrenderstate.md)                     | Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.<br/>                                       |
| [**Setsamplestate**](id3dxeffectstatemanager--setsamplerstate.md)                   | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma amostra.<br/>                                          |
| [**SetTexture**](id3dxeffectstatemanager--settexture.md)                             | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma textura.<br/>                                          |
| [**SetTextureStageState**](id3dxeffectstatemanager--settexturestagestate.md)         | Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.<br/>                            |
| [**SetTransform**](id3dxeffectstatemanager--settransform.md)                         | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma transformação.<br/>                                        |
| [**SetVertexShader**](id3dxeffectstatemanager--setvertexshader.md)                   | Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.<br/>                                    |
| [**SetVertexShaderConstantB**](id3dxeffectstatemanager--setvertexshaderconstantb.md) | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.<br/>        |
| [**SetVertexShaderConstantF**](id3dxeffectstatemanager--setvertexshaderconstantf.md) | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante do sombreador de vértice.<br/> |
| [**SetVertexShaderConstantI**](id3dxeffectstatemanager--setvertexshaderconstanti.md) | Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.<br/>        |



 

## <a name="remarks"></a>Comentários

Um usuário cria uma interface ID3DXEffectStateManager implementando uma classe derivada dessa interface e implementando todos os métodos de interface. Depois que a interface é criada, você pode obter ou definir o Gerenciador de estado dentro de um efeito usando [**ID3DXEffect:: Getstatemanager**](id3dxeffect--getstatemanager.md) e [**ID3DXEffect:: setstatemanager**](id3dxeffect--setstatemanager.md).

O tipo LPD3DXEFFECTSTATEMANAGER é definido como um ponteiro para essa interface.


```
typedef interface ID3DXEffectStateManager ID3DXEffectStateManager;
typedef interface ID3DXEffectStateManager *LPD3DXEFFECTSTATEMANAGER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
