---
title: PSM_ENABLEWIZBUTTONS mensagem (Prsht.h)
description: Habilita ou desabilita qualquer um dos botões padrão em um assistente do Aero. Você pode enviar essa mensagem explicitamente ou usar a \_ macro EnableWizButtons do PropSheet.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS controles Windows mensagem
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
ms.openlocfilehash: a677b596e57a55271224f5b22baac5d979e2806c20676065457aa47b8a66e527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825866"
---
# <a name="psm_enablewizbuttons-message"></a>Mensagem \_ ENABLEWIZBUTTONS do PSM

Habilita ou desabilita qualquer um dos botões padrão em um assistente do Aero. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ EnableWizButtons do PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um ou mais dos valores a seguir que especificam quais botões de folha de propriedades devem ser habilitados. Se um valor de botão for incluído neste parâmetro e *lParam*, ele será habilitado.



| Valor                                                                                                                                                                                 | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ BACK**</dt> </dl>                               | O **botão Voltar.**<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ CANCEL**</dt> </dl>                         | O **botão** Cancelar.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | O **botão** Concluir.<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ FINISH**</dt> </dl>                         | O **botão** Concluir.<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ NEXT**</dt> </dl>                               | O **botão** Próximo.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ou mais dos mesmos valores usados em *wParam*, especificando quais botões são afetados por essa chamada. Se um valor de botão aparecer nesse parâmetro, mas não em *wParam*, isso indicará que o botão deve ser desabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





