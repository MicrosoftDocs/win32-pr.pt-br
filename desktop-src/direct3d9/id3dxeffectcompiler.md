---
description: A interface ID3DXEffectCompiler compila um efeito de uma função ou de um sombreador de vértice.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interface ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298518"
---
# <a name="id3dxeffectcompiler-interface"></a>Interface ID3DXEffectCompiler

A interface **ID3DXEffectCompiler** compila um efeito de uma função ou de um sombreador de vértice.

## <a name="members"></a>Membros

A interface **ID3DXEffectCompiler** herda de [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffectCompiler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXEffectCompiler** tem esses métodos.



| Método                                                      | Descrição                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) | Compile um efeito.<br/>                                                                                                               |
| [**CompileShader**](id3dxeffectcompiler--compileshader.md) | Compila um sombreador de um efeito que contém uma ou mais funções.<br/>                                                            |
| [**Getliteral**](id3dxeffectcompiler--getliteral.md)       | Obtém um status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.<br/>      |
| [**Setliteral**](id3dxeffectcompiler--setliteral.md)       | Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.<br/> |



 

## <a name="remarks"></a>Comentários

A interface ID3DXEffectCompiler é obtida chamando [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)ou [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).

O tipo LPD3DXEFFECTCOMPILER é definido como um ponteiro para essa interface.


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 




