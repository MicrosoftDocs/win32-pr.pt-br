---
description: Retorna um alça de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: Método ID3DXAnimationController::GetUpcomingTrackEvent (D3dx9 multimídia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e2730a9649400af8cc0229cb69ab695044681fde43a29a1a784d212f8d2641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279026"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Método ID3DXAnimationController::GetUpcomingTrackEvent

Retorna um alça de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de faixa.

</dd> <dt>

*hEvent* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

O handle de evento para um evento especificado após o qual pesquisar um evento a seguir. Se definido como **NULL,** o método retornará o próximo evento agendado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

O handle de evento para o próximo evento agendado para ser executado na faixa especificada. **NULL** será retornado se nenhum novo evento for agendado.

## <a name="remarks"></a>Comentários

Esse método pode ser usado iterativamente para localizar um evento desejado passando repetidamente **NULL** para hEvent.

> [!Note]  
> Não itere mais depois que o método tiver retornado **NULL.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
