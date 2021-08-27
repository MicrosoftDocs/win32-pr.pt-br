---
title: Mensagem de TDM_UPDATE_ICON (commctrl. h)
description: Atualiza o ícone de uma caixa de diálogo de tarefa.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- controles de Windows de mensagem de TDM_UPDATE_ICON
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644e214a3edbc420a7aed3d4ba5bc688e6b7af1ed097be325006bb9481e00620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104496"
---
# <a name="tdm_update_icon-message"></a>Mensagem de ícone de \_ atualização TDM \_

Atualiza o ícone de uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Indica qual elemento de ícone deve ser atualizado. Esse parâmetro deve ser um dos seguintes valores:



| Valor                                                                                                                                                                   | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**TDIE \_ ícone \_ principal**</dt> </dl>       | Ícone principal.<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**\_rodapé do ícone de TDIE \_**</dt> </dl> | Ícone de rodapé.<br/> |



 

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres (PCWSTR) ou um identificador para um ícone (HICON) a ser exibido. Se *lParam* for **nulo**, nenhum ícone será exibido, independentemente do valor de *wParam*.

Se o valor de *wParam* for TDIE \_ ícone \_ principal e TDF \_ usar \_ HICON \_ sinalizador principal estiver definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa, *lParam* deverá conter um identificador para um ícone (HICON) a ser exibido.

Se o valor de *wParam* é um \_ rodapé de ícone TDIE \_ e \_ o \_ sinalizador de rodapé usar HICON TDF \_ é definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa, *lParam* deve conter um identificador para um ícone (HICON) a ser exibido.

Se o TDF \_ usar \_ HICON \_ Main ou TDF \_ use \_ HICON \_ sinalizadores de rodapé **não** estiverem definidos no membro **dwFlags** , *lParam* deverá apontar para uma cadeia de caracteres Unicode terminada com NULL (PCWSTR) que contenha um identificador de recurso válido passado pela macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . O ícone é exibido com base no valor de *wParam*: se o valor for TDIE \_ ícone \_ principal, o ícone será exibido no cabeçalho; se o valor for TDIE \_ ícone \_ rodapé, o ícone será exibido no rodapé. O recurso deve ser do módulo de recurso do aplicativo (especificado no membro **HINSTANCE** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) ou, se **HINSTANCE** for **NULL**, do módulo de recurso do sistema (imageres.dll). Para identificar um recurso do sistema, use um identificador de sistema válido passado pela macro **MAKEINTRESOURCE** ou um dos seguintes valores predefinidos de commctrl. h:



| Valor                                                                                                                                                                            | Significado                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**\_ícone de erro TD \_**</dt> </dl>                   | Um ícone de sinal de parada.<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**\_ícone de aviso TD \_**</dt> </dl>             | Um ícone de ponto de exclamação.<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**\_ícone de informações TD \_**</dt> </dl> | Uma letra minúscula "i" em um ícone de círculo.<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**\_ícone de escudo TD \_**</dt> </dl>                | Um ícone de escudo de segurança.<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O layout da caixa de diálogo de tarefa com o ícone pode falhar e isso pode não ser refletido no valor de retorno. Um valor de retorno de S \_ OK reflete apenas que a caixa de diálogo de tarefa recebeu a mensagem e tentou processá-la. Se o layout da caixa de diálogo de tarefa falhar, a caixa de diálogo será fechada e um código **HRESULT** será retornado na função de retorno de chamada registrada. Para obter mais informações sobre a sintaxe da função de retorno de chamada, consulte [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

Se a caixa de diálogo de tarefa for criada sem um rodapé (ou seja, os membros de rodapé apropriados da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usados para criar a caixa de diálogo de tarefa serão **nulos**) e essa mensagem será enviada, um rodapé não será adicionado dinamicamente à caixa de diálogo de tarefa. O mesmo é verdadeiro para enviar essa mensagem para atualizar um ícone de cabeçalho quando uma caixa de diálogo de tarefa é criada sem um cabeçalho. Para adicionar um cabeçalho ou rodapé em tempo de execução, use a funcionalidade de [**\_ \_ página de navegação TDM**](tdm-navigate-page.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

