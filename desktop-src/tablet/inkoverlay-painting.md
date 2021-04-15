---
description: Ocorre antes que o objeto InkOverlay ou InkPicture tenha concluído o redesenho.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. Pintation (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506144"
---
# <a name="inkoverlaypainting-event"></a>Evento InkOverlay. Pintation

Ocorre antes que o objeto [**InkOverlay**](inkoverlay-class.md) ou [InkPicture](inkpicture-control-reference.md) tenha concluído o redesenho.

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

O retângulo que será redesenhado.

</dd> <dt>

*Permitir* \[ entrada, saída\]
</dt> <dd>

Se o redesenho ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEPainting.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

 

 




