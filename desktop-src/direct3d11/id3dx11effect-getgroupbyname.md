---
title: Método ID3DX11Effect GetGroupByName (D3dx11effect.h)
description: Obtém um grupo de efeitos por nome.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Método GetGroupByName Direct3D 11
- Método GetGroupByName Direct3D 11 , interface ID3DX11Effect
- ID3DX11 Interface de efeito Direct3D 11 , método GetGroupByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905fb9fb439dcf613e5abfee22f03bf968c81838c89af17d72e7f4a74d887c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046594"
---
# <a name="id3dx11effectgetgroupbyname-method"></a>Método ID3DX11Effect::GetGroupByName

Obtém um grupo de efeitos por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome do grupo de efeitos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Um ponteiro para uma [**interface ID3DX11EffectGroup.**](id3dx11effectgroup.md)

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

