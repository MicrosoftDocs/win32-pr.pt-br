---
description: Ocorre quando o controle InkPicture é clicado duas vezes.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 515d16d16fb585771a8e2e06e642476b6be7a29851b750add4d6de2ca1a89bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717325"
---
# <a name="inkpicturedblclick-event"></a>Evento InkPicture. DblClick

Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) é clicado duas vezes.

## <a name="syntax"></a>Sintaxe


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cancelar* \[ entrada, saída\]
</dt> <dd>

Se o evento deve ser cancelado para o controle pai.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) . Se houver código no evento de [**clique**](inkpicture-click.md) , o evento **DblClick** nunca será disparado.

 

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEDblClick DISPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




