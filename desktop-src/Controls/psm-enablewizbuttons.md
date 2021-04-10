---
title: Mensagem de PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Habilita ou desabilita qualquer um dos botões padrão em um assistente Aero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Controles de PSM_ENABLEWIZBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918699"
---
# <a name="psm_enablewizbuttons-message"></a>Mensagem de PSM \_ ENABLEWIZBUTTONS

Habilita ou desabilita qualquer um dos botões padrão em um assistente Aero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais dos valores a seguir que especificam quais botões de folha de propriedades devem ser habilitados. Se um valor de botão for incluído nesse parâmetro e no *lParam*, ele será habilitado.



| Valor                                                                                                                                                                                 | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ voltar**</dt> </dl>                               | O botão **voltar** .<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ cancelar**</dt> </dl>                         | O botão **Cancelar** .<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | O botão **concluir** .<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ concluir**</dt> </dl>                         | O botão **concluir** .<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ próximo**</dt> </dl>                               | O botão **Avançar** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ou mais dos mesmos valores usados em *wParam*, especificando quais botões são afetados por essa chamada. Se um valor de botão aparecer nesse parâmetro, mas não em *wParam*, ele indicará que o botão deve ser desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





