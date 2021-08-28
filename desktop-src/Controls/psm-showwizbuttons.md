---
title: Mensagem de PSM_SHOWWIZBUTTONS (Prsht. h)
description: Mostra ou oculta botões em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- controles de Windows de mensagem de PSM_SHOWWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bbad4d6f0ce8a084709c04110d093e4d79b806226bdc1fa651278b4054fa8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088476"
---
# <a name="psm_showwizbuttons-message"></a>Mensagem de PSM \_ SHOWWIZBUTTONS

Mostra ou oculta botões em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais dos valores a seguir que especificam quais botões de folha de propriedades devem ser mostrados. Se um valor de botão for incluído nesse parâmetro e no *lParam*, ele será mostrado.



| Valor                                                                                                                                                                                 | Significado                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ voltar**</dt> </dl>                               | O botão **voltar** .<br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ cancelar**</dt> </dl>                         | O botão **Cancelar** .<br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | O botão **concluir** .<br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ concluir**</dt> </dl>                         | O botão **concluir** .<br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ próximo**</dt> </dl>                               | O botão **Avançar** .<br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <dt>**PSWIZB \_ Mostrar**</dt> </dl>                               | Defina somente este sinalizador (definido como zero) para ocultar todos os botões especificados em *lParam*.<br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <dt>**PSWIZB \_ restauração**</dt> </dl>                      | Não implementado.<br/>                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ou mais dos mesmos valores usados em *wParam*, especificando quais botões são afetados por essa chamada. Se um valor de botão aparecer nesse parâmetro, mas não em *wParam*, o botão ficará oculto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os assistentes exibem três ou quatro botões abaixo de cada página. Essa mensagem é usada para especificar quais botões estão visíveis. Os assistentes normalmente exibem **voltar**, **Cancelar** e um botão **Avançar** ou **concluir** . O botão **Cancelar** está sempre visível.

Normalmente, defina **PSWIZB \_ Finish** ou **PSWIZB \_ DISABLEDFINISH** para substituir o botão **Next** por um botão **Finish** . Para exibir os botões **Avançar** e **concluir** simultaneamente, defina o sinalizador **PSH \_ WIZARDHASFINISH** no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) ao criar o assistente. Cada página exibirá todos os quatro botões: **voltar**, **Avançar**, **Cancelar** e **concluir**.

Se você usar a macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) para enviar essa mensagem, ela será postada. Em qualquer outro momento, você pode usar [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar **\_ SHOWWIZBUTTONS de PSM**.

Se o seu [**manipulador de notificação**](/windows/desktop/api/winuser/nf-winuser-postmessagea) usar a ação executar para enviar uma mensagem de **PSM \_ SHOWWIZBUTTONS** , não faça nada que afete o foco da janela até que o manipulador retorne. Por exemplo, se você chamar [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) imediatamente após usar a Execute para enviar **PSM \_ SHOWWIZBUTTONS**, a **caixa de mensagem** receberá o foco. Como as mensagens postadas não são entregues até chegarem ao início da fila de mensagens, a mensagem de **PSM \_ SHOWWIZBUTTONS** não será entregue até que o assistente tenha perdido o foco na caixa de mensagem. Como resultado, a folha de propriedades não poderá definir corretamente o foco para os botões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

