---
title: Método ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: Obter dados.
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Método GetRawValue Direct3D 11
- Método GetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968672"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a>Método ID3DX11EffectVariable:: GetRawValue

Obter dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **void \***

Um ponteiro para a variável.

</dd> <dt>

*Deslocamento* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O deslocamento (em bytes) desde o início do ponteiro até os dados.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de bytes a serem obtidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Esse método não faz conversão ou verificação de tipo; Portanto, é uma maneira muito rápida de acessar itens de matriz.

> [!Note]  
> O SDK do DirectX não fornece nenhum binário compilado para efeitos. Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

