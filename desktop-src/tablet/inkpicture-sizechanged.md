---
description: Ocorre depois que o controle InkPicture foi reessado, especificamente, após a alteração do valor da propriedade Width ou Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture.SizeChanged (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4473bf580e1683c8d410cd1f2cdbaf271302485f51556b68c4fae7a5d6b99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032034"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture.SizeChanged

Ocorre depois que o [controle InkPicture](inkpicture-control-reference.md) foi reessado, especificamente, após a alteração do valor da propriedade [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)

## <a name="syntax"></a>Sintaxe


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Esquerda* \[ Em\]
</dt> <dd>

A coordenada X do lado esquerdo do [controle InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Superior* \[ Em\]
</dt> <dd>

A coordenada Y da parte superior do [controle InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Direita* \[ Em\]
</dt> <dd>

A coordenada X do lado direito do [controle InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Inferior* \[ Em\]
</dt> <dd>

A coordenada y da parte inferior do [controle InkPicture.](inkpicture-control-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkPictureEvents.** A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador dispID \_ IPESizeChanged.

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

 

