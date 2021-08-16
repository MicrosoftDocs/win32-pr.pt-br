---
title: Método SetBoolArray ID3DX11EffectScalarVariable (D3dx11effect.h)
description: Definir uma matriz de variáveis boolianas.
ms.assetid: 861634a2-547d-497b-b575-bbe6151ade25
keywords:
- Método SetBoolArray Direct3D 11
- Método SetBoolArray Direct3D 11 , interface ID3DX11EffectScalarVariable
- ID3DX11EffectScalarVariable interface Direct3D 11 , método SetBoolArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a095323244cd46526c0df9da23b45a6b0d1e3bdc5e4492a620c734f8745570aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534080"
---
# <a name="id3dx11effectscalarvariablesetboolarray-method"></a>Método ID3DX11EffectScalarVariable::SetBoolArray

Definir uma matriz de variáveis boolianas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pdata* 
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***

Um ponteiro para o início dos dados a definir.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Deve ser definido como 0; isso é reservado para uso futuro.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos de matriz a definir.

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

 

