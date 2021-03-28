---
title: Método ID3DX11EffectType GetMemberTypeByName (D3dx11effect. h)
description: Obter um tipo de membro por nome.
ms.assetid: 0c5a732b-7c3a-41da-b7de-dc464eed814a
keywords:
- Método GetMemberTypeByName Direct3D 11
- Método GetMemberTypeByName Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, método GetMemberTypeByName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e573bcdc2dc4470e87539a307cdc38b71a6320ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989288"
---
# <a name="id3dx11effecttypegetmembertypebyname-method"></a>Método ID3DX11EffectType:: GetMemberTypeByName

Obter um tipo de membro por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectType* GetMemberTypeByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome de um membro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***

Um ponteiro para um [**ID3DX11EffectType**](id3dx11effecttype.md).

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

[ID3DX11EffectType](id3dx11effecttype.md)
</dt> </dl>

 

