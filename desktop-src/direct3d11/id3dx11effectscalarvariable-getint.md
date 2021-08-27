---
title: Método ID3DX11EffectScalarVariable GetInt (D3dx11effect. h)
description: Obter uma variável de inteiro.
ms.assetid: 82a5a7a5-17cb-4e5e-ae4e-57c0ff9757c5
keywords:
- Método GetInt Direct3D 11
- Método GetInt Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, método GetInt
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7619fe4e0fd668e280efa094cc8b8d8d91b2b99f559612bfc6a7af09e08dab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534172"
---
# <a name="id3dx11effectscalarvariablegetint-method"></a>Método ID3DX11EffectScalarVariable:: GetInt

Obter uma variável de inteiro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInt(
   int *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valores* 
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para a variável.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

