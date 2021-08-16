---
title: Mensagem de LVM_SUBITEMHITTEST (commctrl. h)
description: Determina qual item de exibição de lista ou subitem está em uma determinada posição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SubItemHitTest do ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- controles de Windows de mensagem de LVM_SUBITEMHITTEST
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
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830637"
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

## <a name="return-value"></a>Valor retornado

Retorna o índice do item ou subitem testado, se houver, ou-1 caso contrário. Se um item ou subitem estiver nas coordenadas determinadas, os campos da estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) serão preenchidos com as informações de acesso aplicáveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

