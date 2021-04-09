---
title: Mensagem de PSM_SETWIZBUTTONS (Prsht. h)
description: Habilita ou desabilita os botões voltar, avançar e concluir em um assistente. Você também pode usar a \_ macro PropSheet SetWizButtons para postar a mensagem.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Controles de PSM_SETWIZBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085727"
---
# <a name="psm_setwizbuttons-message"></a>Mensagem de PSM \_ SETWIZBUTTONS

Habilita ou desabilita os botões **voltar**, **Avançar** e **concluir** em um assistente. Você também pode usar a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para postar a mensagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Defina esse parâmetro como PSWIZBF \_ ELEVATIONREQUIRED para exibir o ícone com privilégios elevados nos botões especificados em *lParam*. O ícone com privilégios elevados (ou ícone de escudo do UAC) indica que o prompt de elevação será usado para solicitar a aprovação ou as credenciais do usuário. Para obter mais informações, consulte [criando aplicativos de UAC para o Windows Vista]( /previous-versions/bb756973(v=msdn.10)).

> [!Note]  
> Só há suporte para a exibição do ícone de escudo do UAC em AeroWizards (PSH \_ AEROWIZARD).

 

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica quais botões de folha de propriedades estão habilitados. Você pode combinar um ou mais dos sinalizadores a seguir.



| Valor                                                                                                                                                                                 | Significado                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ voltar**</dt> </dl>                               | Habilita o botão **voltar** . Se esse sinalizador não for definido, o botão **voltar** será exibido como desabilitado.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Exibe um botão de **conclusão** desabilitado.<br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ concluir**</dt> </dl>                         | Exibe um botão de **conclusão** habilitado.<br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ próximo**</dt> </dl>                               | Habilita botão **Avançar**. Se esse sinalizador não for definido, o botão **Avançar** será exibido como desabilitado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se o seu [**manipulador de notificação**](/windows/desktop/api/winuser/nf-winuser-postmessagea) usar a ação executar para enviar uma mensagem de **PSM \_ SETWIZBUTTONS** , não faça nada que afete o foco da janela até que o manipulador retorne. Por exemplo, se você chamar [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) imediatamente após usar a Execute para enviar **PSM \_ SETWIZBUTTONS**, a **caixa de mensagem** receberá o foco. Como as mensagens postadas não são entregues até chegarem ao início da fila de mensagens, a mensagem de **PSM \_ SETWIZBUTTONS** não será entregue até que o assistente tenha perdido o foco na caixa de mensagem. Como resultado, a folha de propriedades não poderá definir corretamente o foco para os botões.

Se você enviar a mensagem de PSM \_ SETWIZBUTTONS durante o tratamento da notificação [PSN \_ SetActive](psn-setactive.md) , use a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) em vez da função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . Caso contrário, o sistema não atualizará os botões corretamente. Se você usar a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para enviar essa mensagem, ela será postada. Em qualquer outro momento, você pode usar **SendMessage** para enviar **\_ SETWIZBUTTONS de PSM**.

Os assistentes exibem três ou quatro botões abaixo de cada página. Essa mensagem é usada para especificar quais botões estão habilitados. Os assistentes normalmente exibem **voltar**, **Cancelar** e um botão **Avançar** ou **concluir** . Normalmente, você habilita apenas o botão **Avançar** para a página de boas-vindas, **próximo** e **voltar** para páginas interiores, e **voltar** e **concluir** para a página de conclusão. O botão **Cancelar** está sempre habilitado. Normalmente, definir PSWIZB \_ Finish ou PSWIZB \_ DISABLEDFINISH substitui o botão **Next** por um botão **Finish** . Para exibir os botões **Avançar** e **concluir** simultaneamente, defina o \_ sinalizador PSH WIZARDHASFINISH no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) do assistente ao criar o assistente. Cada página exibirá todos os quatro botões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

