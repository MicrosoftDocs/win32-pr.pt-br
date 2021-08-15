---
title: LVM_GETFOOTERRECT mensagem (Commctrl.h)
description: Recupera as coordenadas do rodapé para um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro ListView GetFooterRect.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT controles de Windows mensagem
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
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411455"
---
# <a name="lvm_getfooterrect-message"></a>Mensagem \_ GETFOOTERRECT LVM

Recupera as coordenadas do rodapé para um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a [**macro \_ ListView GetFooterRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas. O processo de chamada é responsável por alocar essa estrutura. As coordenadas recebidas são expressas como coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

