---
title: Mensagem de LVM_GETSTRINGWIDTH (commctrl. h)
description: Determina a largura de uma cadeia de caracteres especificada usando a fonte atual do controle de exibição de lista especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetStringWidth do ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Controles de LVM_GETSTRINGWIDTH de mensagens do Windows
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
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499666"
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

## <a name="return-value"></a>Retornar valor

Retorna a largura da cadeia de caracteres se for bem-sucedida ou zero caso contrário.

## <a name="remarks"></a>Comentários

A \_ mensagem LVM GETSTRINGWIDTH retorna a largura exata, em pixels, da cadeia de caracteres especificada. Se você usar a largura da cadeia de caracteres retornada como a largura da coluna na mensagem [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , a cadeia de caracteres será truncada. Para recuperar a largura da coluna que pode conter a cadeia de caracteres sem truncar, você deve adicionar o preenchimento à largura da cadeia de caracteres retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





