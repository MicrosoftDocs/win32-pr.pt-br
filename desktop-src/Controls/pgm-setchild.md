---
title: Mensagem de PGM_SETCHILD (commctrl. h)
description: Define a janela contida para o controle de pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- controles de Windows de mensagem de PGM_SETCHILD
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da3424eabfb87d587ac8cd33802dfc03b3c3868d881b131360bfee2e8bc26730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830167"
---
# <a name="pgm_setchild-message"></a>Mensagem de PGM \_

Define a janela contida para o controle de pager. Esta mensagem não vai alterar o pai da janela contida; Ele atribui apenas um identificador de janela ao controle de pager para rolagem. Na maioria dos casos, a janela contida será uma janela filho. Se esse for o caso, a janela contida deverá ser um filho do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetChild do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a janela a ser contida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





