---
title: Mensagem de LVM_SUBITEMHITTEST (commctrl. h)
description: Determina qual item de exibição de lista ou subitem está em uma determinada posição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SubItemHitTest do ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Controles de LVM_SUBITEMHITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454696"
---
# <a name="lvm_subitemhittest-message"></a>\_Mensagem SUBITEMHITTEST LVM

Determina qual item de exibição de lista ou subitem está em uma determinada posição. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SubItemHitTest do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser 0. **Windows Vista.** Deve ser-1 se o membro **iGroup** de *lParam* for recuperado.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) . A estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) em **LVHITTESTINFO** deve ser definida para as coordenadas do cliente para serem testadas com sucesso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item ou subitem testado, se houver, ou-1 caso contrário. Se um item ou subitem estiver nas coordenadas determinadas, os campos da estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) serão preenchidos com as informações de acesso aplicáveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

