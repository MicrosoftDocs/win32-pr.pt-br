---
title: Método ID3DX11EffectScalarVariable SetFloatArray (D3dx11effect. h)
description: Defina uma matriz de variáveis de ponto flutuante.
ms.assetid: af7f3fb1-e5a8-43c9-8c8a-5ee7b3b01242
keywords:
- Método SetFloatArray Direct3D 11
- Método SetFloatArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método SetFloatArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591efd87026caeaadb8de7f29a2741dfccd5028a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930548"
---
# <a name="id3dx11effectscalarvariablesetfloatarray-method"></a>Método ID3DX11EffectScalarVariable:: SetFloatArray

Defina uma matriz de variáveis de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **float \***

Um ponteiro para o início dos dados a serem definidos.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Deve ser definido como 0; Isso é reservado para uso futuro.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos da matriz a serem definidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

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

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

