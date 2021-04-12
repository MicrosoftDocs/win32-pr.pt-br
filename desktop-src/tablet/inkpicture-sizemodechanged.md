---
description: Ocorre depois que a propriedade ModoTamanho do controle InkPicture é alterada.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: Evento InkPicture. Modotamanhochanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297380"
---
# <a name="inkpicturesizemodechanged-event"></a>Evento InkPicture. Modotamanhochanged

Ocorre depois que a propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) do controle [InkPicture](inkpicture-control-reference.md) é alterada.

## <a name="syntax"></a>Sintaxe


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewMode* \[ no\]
</dt> <dd>

O novo estado do controle [InkPicture](inkpicture-control-reference.md) , com base no novo valor da propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> <dt>

*OldMode* \[ no\]
</dt> <dd>

O estado antigo do controle [InkPicture](inkpicture-control-reference.md) , com base no valor antigo da propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPESizeModeChanged DISPID.

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

 

