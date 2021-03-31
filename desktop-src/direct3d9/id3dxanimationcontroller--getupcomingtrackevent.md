---
description: Retorna um identificador de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Método ID3DXAnimationController:: GetUpcomingTrackEvent (D3dx9anim. h)'
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
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930550"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>Método ID3DXAnimationController:: GetUpcomingTrackEvent

Retorna um identificador de evento para o próximo evento agendado para ocorrer após um evento especificado em uma faixa de animação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de faixa.

</dd> <dt>

*hEvent* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para um evento especificado após o qual procurar um evento a seguir. Se definido como **NULL**, o método retornará o próximo evento agendado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para o próximo evento agendado para execução na faixa especificada. **NULL** será retornado se nenhum evento novo estiver agendado.

## <a name="remarks"></a>Comentários

Esse método pode ser usado iterativamente para localizar um evento desejado, passando repetidamente em **NULL** para hEvent.

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

 

 
