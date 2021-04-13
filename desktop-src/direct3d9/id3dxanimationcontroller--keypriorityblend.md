---
description: Define as chaves de evento de mesclagem para a faixa de animação especificada.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Método ID3DXAnimationController:: KeyPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298501"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>Método ID3DXAnimationController:: KeyPriorityBlend

Define as chaves de evento de mesclagem para a faixa de animação especificada.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewBlendWeight* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Número entre 0 e 1 que é usado para mesclar faixas.

</dd> <dt>

*StartTime* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Tempo global para iniciar o Blend.

</dd> <dt>

*Duração* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Duração de tempo global do Blend.

</dd> <dt>

*Transição* \[ no\]
</dt> <dd>

Tipo: **[ **\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md)**

Especifica o tipo de transição usado para a duração do Blend. Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o evento de mesclagem de prioridade. **NULL** será retornado se um ou mais dos parâmetros de entrada forem inválidos ou se nenhum evento gratuito estiver disponível.

## <a name="remarks"></a>Comentários

O controlador de animação combina em três fases: as faixas de baixa prioridade são mescladas primeiro, as faixas de alta prioridade são mescladas segundo e, em seguida, os resultados de ambos são misturados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
