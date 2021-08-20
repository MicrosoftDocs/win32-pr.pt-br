---
title: Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Obtenha uma técnica por nome. | Método ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Método GetTechniqueByName Direct3D 11
- Método GetTechniqueByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62822789746cc9eb120d5102de12f8bc8174fa010db1bbdfff62119685390cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808119"
---
# <a name="id3dx11effectgettechniquebyname-method"></a>Método ID3DX11Effect:: GetTechniqueByName

Obtenha uma técnica por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome da técnica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Um ponteiro para um [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md). Se uma técnica com o nome apropriado não for encontrada, uma técnica inválida será retornada. [**ID3DX11EffectTechnique:: IsValid**](id3dx11effecttechnique-isvalid.md) deve ser chamado na técnica retornada para determinar se ele é válido.

## <a name="remarks"></a>Comentários

Um efeito contém uma ou mais técnicas; cada técnica contém uma ou mais passagens. Você pode acessar uma técnica usando seu nome ou com um índice.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

