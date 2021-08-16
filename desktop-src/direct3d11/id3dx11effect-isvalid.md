---
title: Método ID3DX11Effect IsValid (D3dx11effect.h)
description: Teste um efeito para ver se ele contém sintaxe válida. | Método ID3DX11Effect IsValid (D3dx11effect.h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11 , interface ID3DX11Effect
- ID3DX11 Interface de efeito Direct3D 11 , método IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d49cff0f745caddf571b0f0e8d3d2d351d8a90058335611c43edd89f79d84810
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608786"
---
# <a name="id3dx11effectisvalid-method"></a>Método ID3DX11Effect::IsValid

Teste um efeito para ver se ele contém sintaxe válida.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** se a sintaxe de código for válida; caso **contrário, FALSE.**

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

 

