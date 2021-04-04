---
title: Mensagem de PGM_SETCHILD (commctrl. h)
description: Define a janela contida para o controle de pager.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Controles de PGM_SETCHILD de mensagens do Windows
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
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085461"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





