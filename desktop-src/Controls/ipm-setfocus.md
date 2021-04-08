---
title: Mensagem de IPM_SETFOCUS (commctrl. h)
description: Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- Controles de IPM_SETFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085816"
---
# <a name="ipm_setfocus-message"></a>\_Mensagem IPM SETFOCUS

Define o foco do teclado para o campo especificado no controle de endereço IP. Todo o texto nesse campo será selecionado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um índice de campo baseado em zero ao qual o foco deve ser definido. Se esse valor for maior que o número de campos, o foco será definido como o primeiro campo em branco. Se todos os campos não estiverem em branco, o foco será definido como o primeiro campo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





