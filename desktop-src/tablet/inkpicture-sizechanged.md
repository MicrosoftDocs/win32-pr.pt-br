---
description: Ocorre depois que o controle InkPicture é redimensionado, especificamente, depois que o valor da propriedade Width ou Height é alterado.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922649"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture. SizeChanged

Ocorre depois que o controle [InkPicture](inkpicture-control-reference.md) é redimensionado, especificamente, depois que o valor da propriedade [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) é alterado.

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

*À esquerda* \[ no\]
</dt> <dd>

A coordenada x do lado esquerdo do controle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*Superior* \[ no\]
</dt> <dd>

A coordenada y da parte superior do controle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*À direita* \[ no\]
</dt> <dd>

A coordenada x do lado direito do controle [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*Parte inferior* \[ no\]
</dt> <dd>

A coordenada y da parte inferior do controle [InkPicture](inkpicture-control-reference.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPESizeChanged DISPID.

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

 

