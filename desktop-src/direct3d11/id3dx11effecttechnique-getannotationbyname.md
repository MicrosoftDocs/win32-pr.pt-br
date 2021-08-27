---
title: Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
description: Obter uma anotação por nome. | Método ID3DX11EffectTechnique GetAnnotationByName (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ba87c400129d9caab88657f0d554c67a75072feaf425054ee638ccf7b3d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069656"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a>Método ID3DX11EffectTechnique:: GetAnnotationByName

Obter uma anotação por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome da anotação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Um ponteiro para um [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Comentários

Use uma anotação para anexar uma parte dos metadados a uma técnica.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

