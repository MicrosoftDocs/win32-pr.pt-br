---
title: Mensagem de LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterItemRect do ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- controles de Windows de mensagem de LVM_GETFOOTERITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5df635c18de3dec7cad128fe23ceeea2829b273984c561f5f289e2f0533b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830667"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Mensagem GETFOOTERITEMRECT LVM

Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterItemRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice do item no controle de exibição de lista.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas. O aplicativo de chamada é responsável por alocar essa estrutura. As coordenadas recebidas são expressas como coordenadas do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

