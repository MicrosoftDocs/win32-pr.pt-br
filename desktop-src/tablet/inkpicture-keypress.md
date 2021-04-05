---
description: Ocorre quando uma tecla é pressionada enquanto o controle InkPicture tem foco.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Evento InkPicture. KeyPress (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921025"
---
# <a name="inkpicturekeypress-event"></a>Evento InkPicture. KeyPress

Ocorre quando uma tecla é pressionada enquanto o controle [InkPicture](inkpicture-control-reference.md) tem foco.

## <a name="syntax"></a>Sintaxe


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeyAscii* \[ entrada, saída\]
</dt> <dd>

O valor ASCII da chave que está sendo pressionada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEKeyPress DISPID.

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

 

