---
title: Mensagem de WM_NOTIFYFORMAT (WinUser. h)
description: Determina se uma janela aceita estruturas ANSI ou Unicode na mensagem de \_ notificação do WM Notify. \_As mensagens do WM NOTIFYFORMAT são enviadas de um controle comum para sua janela pai e da janela pai para o controle comum.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Controles de WM_NOTIFYFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918691"
---
# <a name="wm_notifyformat-message"></a>Mensagem do WM \_ NOTIFYFORMAT

Determina se uma janela aceita estruturas ANSI ou Unicode na mensagem de notificação do [**WM \_ Notify**](wm-notify.md) . **WM \_** As mensagens NOTIFYFORMAT são enviadas de um controle comum para sua janela pai e da janela pai para o controle comum.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que está enviando a **mensagem \_ NOTIFYFORMAT do WM** . Se *lParam* for NF \_ , esse parâmetro será o identificador para um controle. Se *lParam* for NF \_ RepetirConsulta, esse parâmetro será o identificador para a janela pai de um controle.

</dd> <dt>

*lParam* 
</dt> <dd>

O valor do comando que especifica a natureza da mensagem do **WM \_ NOTIFYFORMAT** . Esse será um dos seguintes valores:



| Valor                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**consulta de NF \_**</dt> </dl>       | A mensagem é uma consulta para determinar se as estruturas ANSI ou Unicode devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) . Esse comando é enviado de um controle para sua janela pai durante a criação de um controle e em resposta a um comando de NF- \_ repetição.<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**reconsulta de NF \_**</dt> </dl> | A mensagem é uma solicitação de um controle para enviar um \_ formulário de consulta de NF dessa mensagem para sua janela pai. Esse comando é enviado da janela pai. A janela pai está solicitando que o controle refaça a consulta sobre o tipo de estruturas a serem usadas nas mensagens de [**\_ notificação do WM**](wm-notify.md) . Se *lParam* for NF \_ RepetirConsulta, o valor de retorno será o resultado da operação de consulta.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                                 | Descrição                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NFR \_ ANSI**</dt> </dl>    | As estruturas ANSI devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) enviadas pelo controle.<br/>     |
| <dl> <dt>**NFR \_ Unicode**</dt> </dl> | As estruturas Unicode devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) enviadas pelo controle. <br/> |
| <dl> <dt>**0**</dt> </dl>            | Ocorreu um erro.<br/>                                                                                  |



 

## <a name="remarks"></a>Comentários

Quando um controle comum é criado, o controle envia uma mensagem do **WM \_ NOTIFYFORMAT** para sua janela pai para determinar o tipo de estruturas a serem usadas nas mensagens de [**\_ notificação do WM**](wm-notify.md) . Se a janela pai não tratar essa mensagem, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) responderá de acordo com o tipo da janela pai. Ou seja, se a janela pai for uma janela Unicode, **DefWindowProc** retornará NFR \_ Unicode e, se a janela pai for uma janela ANSI, **DefWindowProc** retornará NFR \_ ANSI. Se a janela pai for uma caixa de diálogo e não tratar essa mensagem, a função [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) responderá de acordo com o tipo da caixa de diálogo (Unicode ou ANSI).

Uma janela pai pode alterar o tipo de estruturas que um controle comum usa no [**WM \_ notificar**](wm-notify.md) mensagens definindo *lParam* para NF \_ RepetirConsulta e enviando uma mensagem do **WM \_ NOTIFYFORMAT** para o controle. Isso faz com que o controle envie um \_ formulário de consulta de NF da mensagem do **WM \_ NOTIFYFORMAT** para a janela pai.

Todos os controles comuns enviarão mensagens do **WM \_ NOTIFYFORMAT** . No entanto, os controles padrão do Windows (editar controles, caixas de combinação, caixas de listagem, botões, barras de rolagem e controles estáticos) não fazem isso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



 

