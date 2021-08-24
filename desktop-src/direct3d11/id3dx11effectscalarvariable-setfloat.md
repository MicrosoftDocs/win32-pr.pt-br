---
title: Método SetFloat ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Definir uma variável de ponto flutuante.
ms.assetid: e13f3ba1-437a-47f0-bd08-4423ffc25ddb
keywords:
- Método SetFloat Direct3D 11
- Método SetFloat Direct3D 11 , interface ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , método SetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573880f07752e353e7a623d249353f7e0f020902443fde23538f38a2227e7d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460846"
---
# <a name="id3dx11effectscalarvariablesetfloat-method"></a>Método ID3DX11EffectScalarVariable::SetFloat

Definir uma variável de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFloat(
   float Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valor* 
</dt> <dd>

Tipo: **float**

Um ponteiro para a variável.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





