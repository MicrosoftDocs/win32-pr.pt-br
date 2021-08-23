---
description: Ocorre antes que o controle InkPicture redesenhar a si mesmo.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture.Painting (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129e5f74ee8097794112b70fb709ab9b9a3b8fadc9f3e5a2fd7d874c65c0d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966965"
---
# <a name="inkpicturepainting-event"></a>Evento InkPicture.Painting

Ocorre antes que o [controle InkPicture](inkpicture-control-reference.md) redesenhar a si mesmo.

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

*hDC* \[ Em\]
</dt> <dd>

O contexto do dispositivo no qual a pintura ocorrerá.

</dd> <dt>

*Rect* \[ Em\]
</dt> <dd>

O retângulo de tinta que deve ser repintado.

</dd> <dt>

*Permitir* \[ in, out\]
</dt> <dd>

Se a reint ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de \_ IOEPainting DISPID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




