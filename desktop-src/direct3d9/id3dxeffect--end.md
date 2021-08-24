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
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748656"
---
# <a name="id3dxeffectend-method"></a>Método ID3DXEffect:: End

Termina uma técnica ativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

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

 

 




