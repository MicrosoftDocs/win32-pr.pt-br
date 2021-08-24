---
title: Método ID3DX11Effect GetConstantBufferByIndex (D3dx11effect.h)
description: Obter um buffer constante por índice.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Método GetConstantBufferByIndex Direct3D 11
- Método GetConstantBufferByIndex Direct3D 11 , interface ID3DX11Effect
- ID3DX11 Interface de efeito Direct3D 11 , método GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d2ce34bb6bde85600e57182151e8c270885e60f919f22a723228b14dd17927a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632596"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>Método ID3DX11Effect::GetConstantBufferByIndex

Obter um buffer constante por índice.

## <a name="syntax"></a>Sintaxe


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um índice baseado em zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Um ponteiro para um [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Comentários

Um efeito que contém uma variável que será lida/escrita por um aplicativo requer pelo menos um buffer constante. Para obter o melhor desempenho, um efeito deve organizar variáveis em um ou mais buffers constantes com base na frequência de atualização.

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

 

