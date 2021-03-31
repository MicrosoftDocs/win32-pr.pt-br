---
description: Retorna um identificador de evento para o próximo evento de mesclagem de prioridade agendado para ocorrer após um evento especificado.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Método ID3DXAnimationController:: GetUpcomingPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370918"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a>Método ID3DXAnimationController:: GetUpcomingPriorityBlend

Retorna um identificador de evento para o próximo evento de mesclagem de prioridade agendado para ocorrer após um evento especificado.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hEvent* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para um evento especificado após o qual procurar um evento de mesclagem de prioridade a seguir. Se definido como **NULL**, o método retornará o próximo evento de mesclagem de prioridade agendado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o próximo evento de mesclagem de prioridade agendado. **NULL** será retornado se nenhum evento de mesclagem de prioridade novo estiver agendado.

## <a name="remarks"></a>Comentários

Esse método pode ser usado iterativamente para localizar um evento de mesclagem de prioridade desejado, passando repetidamente em **NULL** para hEvent.

> [!Note]  
> Não iterar mais após o método ter retornado **NULL**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




