---
description: Ocorre quando o controle InkPicture é clicado duas vezes.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297226"
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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) . Se houver código no evento de [**clique**](inkpicture-click.md) , o evento **DblClick** nunca será disparado.

 

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEDblClick DISPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




