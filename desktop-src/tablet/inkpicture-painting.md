---
description: Ocorre antes de o controle InkPicture ser redesenhado.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture. Pintation (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170076"
---
# <a name="inkpicturepainting-event"></a>Evento InkPicture. Pintation

Ocorre antes de o controle [InkPicture](inkpicture-control-reference.md) ser redesenhado.

## <a name="syntax"></a>Sintaxe


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

O contexto do dispositivo no qual a pintura ocorrerá.

</dd> <dt>

*Rect* \[ no\]
</dt> <dd>

O retângulo de tinta que deve ser redesenhado.

</dd> <dt>

*Permitir* \[ entrada, saída\]
</dt> <dd>

Se o redesenho ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOEPainting.

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

 

 




