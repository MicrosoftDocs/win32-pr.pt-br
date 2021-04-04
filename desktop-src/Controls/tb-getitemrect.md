---
title: Mensagem de TB_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador de um botão em uma barra de ferramentas.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Controles de TB_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824617"
---
# <a name="tb_getitemrect-message"></a>TB de \_ mensagem GETITEMRECT

Recupera o retângulo delimitador de um botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero do botão para o qual recuperar informações.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe as coordenadas de cliente do retângulo delimitador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esta mensagem não recupera o retângulo delimitador para botões cujo estado é definido como o [**valor \_ oculto TBSTATE**](toolbar-button-states.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

