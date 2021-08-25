---
title: BM_GETIMAGE mensagem (Winuser.h)
description: Recupera um alça para a imagem (ícone ou bitmap) associada ao botão.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE controles Windows mensagem
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b98ede304499aa97d9129957aa69a0991dee98565ff7827cdad4d0c1a82f19b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921256"
---
# <a name="bm_getimage-message"></a>Mensagem \_ GETIMAGE BM

Recupera um alça para a imagem (ícone ou bitmap) associada ao botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de imagem a ser associado ao botão. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                      | Significado              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP \_ DE IMAGEM**</dt> </dl> | Um bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ÍCONE DE \_ IMAGEM**</dt> </dl>       | Um ícone.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um handle para a imagem, se for o caso; caso contrário, será **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BM \_ SETIMAGE**](bm-setimage.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Botões](buttons.md)
</dt> </dl>

 

 





