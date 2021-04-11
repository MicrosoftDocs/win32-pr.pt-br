---
title: Mensagem de BM_GETIMAGE (WinUser. h)
description: Recupera um identificador para a imagem (ícone ou bitmap) associado ao botão.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Controles de BM_GETIMAGE de mensagens do Windows
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
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295842"
---
# <a name="bm_getimage-message"></a>\_Mensagem BM GETimage

Recupera um identificador para a imagem (ícone ou bitmap) associado ao botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de imagem a ser associado ao botão. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                      | Significado              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**BITMAP de imagem \_**</dt> </dl> | Um bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ícone de imagem \_**</dt> </dl>       | Um ícone.<br/>  |



 

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

**Referência**
</dt> <dt>

[**BM \_ SETimage**](bm-setimage.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Botões](buttons.md)
</dt> </dl>

 

 





