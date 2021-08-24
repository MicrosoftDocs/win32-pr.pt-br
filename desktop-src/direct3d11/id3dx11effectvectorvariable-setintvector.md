---
title: Método SetIntVector ID3DX11EffectVectorVariable (D3dx11effect.h)
description: Definir um vetor de quatro componentes que contém dados inteiros.
ms.assetid: d0546da4-c3b4-4e97-9aa9-d3b7022e22c5
keywords:
- Método SetIntVector Direct3D 11
- Método SetIntVector Direct3D 11 , interface ID3DX11EffectVectorVariable
- ID3DX11EffectVectorVariable interface Direct3D 11 , método SetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9c388ec72beb4ce9be7356c3b1485d58e6dca0508b84a5dd5ff3566850c4ab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791806"
---
# <a name="id3dx11effectvectorvariablesetintvector-method"></a>Método ID3DX11EffectVectorVariable::SetIntVector

Definir um vetor de quatro componentes que contém dados inteiros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetIntVector(
   int *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pdata* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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

 

