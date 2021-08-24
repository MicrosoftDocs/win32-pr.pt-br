---
title: Método GetFloat ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Obter uma variável de ponto flutuante.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Método GetFloat Direct3D 11
- Método GetFloat Direct3D 11 , interface ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , método GetFloat
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f00e5f4863b54a208b1b9f9b32e4292c274575271e447c3ac20e7b09a686ace
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952716"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>Método ID3DX11EffectScalarVariable::GetFloat

Obter uma variável de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pvalue* 
</dt> <dd>

Tipo: **\* float**

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

 

 





