---
title: Método ID3DX11EffectType GetMemberTypeBySemantic (D3dx11effect.h)
description: Obter um tipo de membro por semântica.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Método GetMemberTypeBySemantic Direct3D 11
- Método GetMemberTypeBySemantic Direct3D 11 , interface ID3DX11EffectType
- ID3DX11EffectType interface Direct3D 11 , método GetMemberTypeBySemantic
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e1add6ddc485f803512050795b9ba240f2a29d145fb01e864b88bc8ba84ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532328"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a>Método ID3DX11EffectType::GetMemberTypeBySemantic

Obter um tipo de membro por semântica.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Semântica* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Uma semântica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Um ponteiro para um [**ID3DX11EffectType**](id3dx11effecttype.md).

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

