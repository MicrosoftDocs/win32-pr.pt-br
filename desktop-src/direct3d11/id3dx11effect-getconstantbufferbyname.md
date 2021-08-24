---
title: Método ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtenha um buffer constante por nome.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Método GetConstantBufferByName Direct3D 11
- Método GetConstantBufferByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400be04e6955807bb6b2a60e712323f8993e55ecc031086afb3597f3962091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632556"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>Método ID3DX11Effect:: GetConstantBufferByName

Obtenha um buffer constante por nome.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

O nome do buffer de constantes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Um ponteiro para o buffer de constantes indicado pelo nome. Consulte [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Comentários

Um efeito que contém uma variável que será lida/gravada por um aplicativo requer pelo menos um buffer constante. Para obter um melhor desempenho, um efeito deve organizar variáveis em um ou mais buffers constantes com base em sua frequência de atualização.

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

 

