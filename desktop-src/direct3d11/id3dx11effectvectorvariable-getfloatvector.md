---
title: Método GetFloatVector ID3DX11EffectVectorVariable (D3dx11effect.h)
description: Obter um vetor de quatro componentes que contém dados de ponto flutuante.
ms.assetid: 980c85db-0d40-49e0-99d0-5049fdf62540
keywords:
- Método GetFloatVector Direct3D 11
- Método GetFloatVector Direct3D 11 , interface ID3DX11EffectVectorVariable
- ID3DX11EffectVectorVariable interface Direct3D 11 , método GetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 861121c89bbeda277610c0c3e42d4d6e41795b5cd82b48ae8ba42a1783ee5eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989666"
---
# <a name="id3dx11effectvectorvariablegetfloatvector-method"></a>Método ID3DX11EffectVectorVariable::GetFloatVector

Obter um vetor de quatro componentes que contém dados de ponto flutuante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pdata* 
</dt> <dd>

Tipo: **\* float**

Um ponteiro para o primeiro componente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





