---
title: Mensagem de STM_GETIMAGE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem STM GetImage para recuperar um identificador para a imagem (ícone ou bitmap) associado a um controle estático.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Controles de STM_GETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008921"
---
# <a name="stm_getimage-message"></a>\_Mensagem de GETIMAGE STM

Um aplicativo envia uma mensagem **STM \_ GetImage** para recuperar um identificador para a imagem (ícone ou bitmap) associado a um controle estático.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de imagem a recuperar. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP de imagem \_**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**CURSOR de imagem \_**</dt> </dl>                | Posição.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**ENHMETAFILE de imagem \_**</dt> </dl> | Metarquivo avançado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ícone de imagem \_**</dt> </dl>                      | Cone.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um identificador para a imagem, se houver; caso contrário, será **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_imagem STM**](stm-setimage.md)
</dt> </dl>

 

 





