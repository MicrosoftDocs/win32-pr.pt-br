---
description: Termina uma técnica ativa.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'Método ID3DXEffect:: End (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298652"
---
# <a name="id3dxeffectend-method"></a>Método ID3DXEffect:: End

Termina uma técnica ativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método sempre retorna o valor S \_ OK.

## <a name="remarks"></a>Comentários

Toda a renderização em um efeito é feita dentro de um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e **ID3DXEffect:: End** calls. Depois que todas as passagens são renderizadas, **ID3DXEffect:: End** deve ser chamado para encerrar a técnica ativa. O sistema de efeitos responde usando o bloco de estado criado quando **ID3DXEffect:: Begin** foi chamado, para restaurar automaticamente o estado do pipeline antes de **ID3DXEffect:: Begin**.

Por padrão, o sistema de efeitos cuida do salvamento do estado antes de uma técnica e da restauração do estado após uma técnica. Se você optar por desabilitar essa funcionalidade de salvar e restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




