---
description: Ocorre quando uma tecla é pressionada enquanto o controle InkPicture tem foco.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture.KeyPress (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7545b0de722ec9b48c66aa5d2236bf81eb576d87916c15e618508e537981a2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939006"
---
# <a name="inkpicturekeypress-event"></a>Evento InkPicture.KeyPress

Ocorre quando uma tecla é pressionada enquanto o [controle InkPicture](inkpicture-control-reference.md) tem foco.

## <a name="syntax"></a>Sintaxe


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeyAscii* \[ in, out\]
</dt> <dd>

O valor ASCII da chave que está sendo pressionada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkPictureEvents.** A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ DISPID IPEKeyPress.

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

 

