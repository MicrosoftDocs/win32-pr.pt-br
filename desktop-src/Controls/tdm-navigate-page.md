---
title: Mensagem de TDM_NAVIGATE_PAGE (commctrl. h)
description: Recria uma caixa de diálogo de tarefa com novo conteúdo, simulando a funcionalidade de um assistente de várias páginas.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- controles de Windows de mensagem de TDM_NAVIGATE_PAGE
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7894bdc5831af2c1fe2e779679aaab38eab94f976cf9c586dfe64d26a051b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104626"
---
# <a name="tdm_navigate_page-message"></a>\_ \_ Mensagem da página de navegação TDM

Recria uma caixa de diálogo de tarefa com novo conteúdo, simulando a funcionalidade de um assistente de várias páginas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Não usado. Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que descreve a caixa de diálogo de tarefa a ser criada. O aplicativo de chamada deve alocar essa estrutura e definir seus membros. Os valores dos membros variam dependendo do tipo de página para a qual o usuário navega.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para iniciar uma caixa de diálogo de tarefa do assistente, use a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . À medida que o usuário navega usando o assistente, envie essa mensagem para a caixa de diálogo de tarefa para exibir a próxima página. Uma caixa de diálogo Nova tarefa (semelhante a uma nova página) é criada com os elementos especificados na estrutura apontada por *lParam*. Na criação, todo o conteúdo do quadro da caixa de diálogo é destruído e reconstruído. Como resultado, todas as informações de estado mantidas pelos controles (por exemplo, uma barra de progresso, um botão expando ou uma caixa de seleção de verificação) na caixa de diálogo são perdidas.

O layout da caixa de diálogo de tarefa pode falhar e isso pode não ser refletido no valor de retorno. Um valor de retorno de S \_ OK reflete apenas que a caixa de diálogo de tarefa recebeu a mensagem e tentou processá-la. Se o layout da caixa de diálogo de tarefa falhar (a caixa de diálogo de tarefa não pode ser exibida), a caixa de diálogo será fechada e um código **HRESULT** será retornado na função de retorno de chamada registrada. Para obter mais informações sobre a sintaxe da função de retorno de chamada, consulte [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

