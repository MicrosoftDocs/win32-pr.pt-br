---
title: Mensagem de TB_INSERTMARKHITTEST (commctrl. h)
description: Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- controles de Windows de mensagem de TB_INSERTMARKHITTEST
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc231b915d6d71cc22ee3cd98b1c6dd602451cc3c70d2153ba1bee8a0d55657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061356"
---
# <a name="tb_insertmarkhittest-message"></a>TB de \_ mensagem INSERTMARKHITTEST

Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que contém as coordenadas de teste de clique, em relação à área do cliente da barra de ferramentas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recebe as informações de marca de inserção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se o ponto for uma marca de inserção, ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

