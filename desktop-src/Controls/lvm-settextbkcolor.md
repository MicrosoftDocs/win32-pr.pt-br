---
title: Mensagem de LVM_SETTEXTBKCOLOR (commctrl. h)
description: Define a cor da tela de fundo do texto em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTextBkColor do ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- controles de Windows de mensagem de LVM_SETTEXTBKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656226"
---
# <a name="lvm_settextbkcolor-message"></a>\_Mensagem SETTEXTBKCOLOR LVM

Define a cor da tela de fundo do texto em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nova cor do plano de fundo do texto. Isso pode ser \_ nenhum CLR para nenhuma cor do plano de fundo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





