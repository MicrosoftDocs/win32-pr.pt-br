---
title: Função D3DX11CreateEffectFromMemory (D3dx11effect. h)
description: Cria um efeito de um arquivo ou efeito binário.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Função D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989341"
---
# <a name="d3dx11createeffectfrommemory-function"></a>Função D3DX11CreateEffectFromMemory

Cria um efeito de um arquivo ou efeito binário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **void \***

Blob de dados de efeito compilados.

</dd> <dt>

*DataLength* 
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Comprimento do blob de dados.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Não existem sinalizadores de efeito. Definido como zero.

</dd> <dt>

*pDevice* 
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Ponteiro para o [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) no qual criar recursos de efeito.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Tipo: **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Endereço da interface [**ID3DX11Effect**](id3dx11effect.md) recém-criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Você deve usar a [fonte Effects 11](https://github.com/Microsoft/FX11) para criar seu aplicativo de tipo de efeitos. Para obter mais informações sobre como usar a fonte de efeitos 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções do Effects 11](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

