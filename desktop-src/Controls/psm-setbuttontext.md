---
title: Mensagem de PSM_SETBUTTONTEXT (Prsht. h)
description: Define o texto em um botão em um assistente de Aero. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Controles de PSM_SETBUTTONTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009260"
---
# <a name="psm_setbuttontext-message"></a>Mensagem de PSM \_ SETBUTTONTEXT

Define o texto em um botão em um assistente de Aero. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um dos valores a seguir especificando o botão cujo texto está definido.



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

O texto a ser definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





