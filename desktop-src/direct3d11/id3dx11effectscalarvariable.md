---
title: Interface ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Uma interface de variável escalar de efeito acessa valores escalares.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Interface ID3DX11EffectScalarVariable Direct3D 11
- Interface ID3DX11EffectScalarVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172934"
---
# <a name="id3dx11effectscalarvariable-interface"></a>Interface ID3DX11EffectScalarVariable

Uma interface de variável escalar de efeito acessa valores escalares.

## <a name="members"></a>Membros

A interface **ID3DX11EffectScalarVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11EffectScalarVariable** tem esses métodos.



| Método                                                             | Descrição                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**Getbool**](id3dx11effectscalarvariable-getbool.md)             | Obter uma variável booliana.<br/>                   |
| [**GetBoolArray**](id3dx11effectscalarvariable-getboolarray.md)   | Obter uma matriz de variáveis booleanas.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Obter uma variável de ponto flutuante.<br/>            |
| [**GetFloatArray**](id3dx11effectscalarvariable-getfloatarray.md) | Obter uma matriz de variáveis de ponto flutuante.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Obter uma variável de inteiro.<br/>                  |
| [**GetIntArray**](id3dx11effectscalarvariable-getintarray.md)     | Obter uma matriz de variáveis de inteiro.<br/>        |
| [**Setbool**](id3dx11effectscalarvariable-setbool.md)             | Defina uma variável booliana.<br/>                   |
| [**SetBoolArray**](id3dx11effectscalarvariable-setboolarray.md)   | Defina uma matriz de variáveis boolianas.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Defina uma variável de ponto flutuante.<br/>            |
| [**SetFloatArray**](id3dx11effectscalarvariable-setfloatarray.md) | Defina uma matriz de variáveis de ponto flutuante.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Defina uma variável de inteiro.<br/>                  |
| [**SetIntArray**](id3dx11effectscalarvariable-setintarray.md)     | Defina uma matriz de variáveis de inteiro.<br/>        |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efeitos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





