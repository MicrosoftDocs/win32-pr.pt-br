---
title: Mensagem de LVM_GETSTRINGWIDTH (commctrl. h)
description: Determina a largura de uma cadeia de caracteres especificada usando a fonte atual do controle de exibição de lista especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetStringWidth do ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- controles de Windows de mensagem de LVM_GETSTRINGWIDTH
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019304"
---
# <a name="lvm_getstringwidth-message"></a>\_Mensagem GETSTRINGWIDTH LVM

Determina a largura de uma cadeia de caracteres especificada usando a fonte atual do controle de exibição de lista especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetStringWidth do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a largura da cadeia de caracteres se for bem-sucedida ou zero caso contrário.

## <a name="remarks"></a>Comentários

A \_ mensagem LVM GETSTRINGWIDTH retorna a largura exata, em pixels, da cadeia de caracteres especificada. Se você usar a largura da cadeia de caracteres retornada como a largura da coluna na mensagem [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , a cadeia de caracteres será truncada. Para recuperar a largura da coluna que pode conter a cadeia de caracteres sem truncar, você deve adicionar o preenchimento à largura da cadeia de caracteres retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





