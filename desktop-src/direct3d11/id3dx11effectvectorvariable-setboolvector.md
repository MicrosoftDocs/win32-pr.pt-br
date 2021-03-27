---
title: Método ID3DX11EffectVectorVariable SetBoolVector (D3dx11effect. h)
description: Defina um vetor de quatro componentes que contém dados boolianos.
ms.assetid: 2138eeb9-6aa0-43f5-852c-1ab9c8117a88
keywords:
- Método SetBoolVector Direct3D 11
- Método SetBoolVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, método SetBoolVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03cc5885353e59d3c95139dcd7d99ce39c6f1015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930691"
---
# <a name="id3dx11effectvectorvariablesetboolvector-method"></a>Método ID3DX11EffectVectorVariable:: SetBoolVector

Defina um vetor de quatro componentes que contém dados boolianos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para o primeiro componente.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

