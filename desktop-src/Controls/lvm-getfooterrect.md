---
title: Mensagem de LVM_GETFOOTERRECT (commctrl. h)
description: Recupera as coordenadas do rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterRect do ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Controles de LVM_GETFOOTERRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085170"
---
# <a name="lvm_getfooterrect-message"></a>\_Mensagem GETFOOTERRECT LVM

Recupera as coordenadas do rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser 0.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas. O processo de chamada é responsável por alocar essa estrutura. As coordenadas recebidas são expressas como coordenadas do cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

