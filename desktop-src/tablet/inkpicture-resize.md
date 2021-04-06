---
description: Ocorre quando o controle InkPicture é redimensionado (quando os valores de propriedade Width e/ou Height são alterados).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011480"
---
# <a name="inkpictureresize-event"></a>Evento InkPicture. Resize

Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) é redimensionado (quando os valores de propriedade Width e/ou Height são alterados).

## <a name="syntax"></a>Sintaxe


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mantida* 
</dt> <dd>

O número de pixels do lado esquerdo da janela que contém o controle para o lado esquerdo do controle.

</dd> <dt>

*Top* 
</dt> <dd>

O número de pixels da parte superior da janela que contém o controle até a parte superior do controle.

</dd> <dt>

*Certo* 
</dt> <dd>

O número de pixels do lado esquerdo da janela que contém o controle do lado direito do controle.

</dd> <dt>

*Inferior* 
</dt> <dd>

O número de pixels da parte superior da janela que contém o controle até a parte inferior do controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

A nova largura do controle em pixels será igual à diferença entre os parâmetros *direito* e *esquerdo* . Da mesma forma, a nova altura será igual à diferença entre *inferior* e *superior*.

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEResize DISPID**.

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

 

 




