---
title: PSM_SETBUTTONTEXT mensagem (Prsht.h)
description: Define o texto em um botão em um assistente do Aero. Você pode enviar essa mensagem explicitamente ou usando a macro \_ PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT controles de Windows mensagem
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
ms.openlocfilehash: feac193beef3149140447a38c0be00b7f4fa0c1c1b28e10a5d7de2203ba21cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088586"
---
# <a name="psm_setbuttontext-message"></a>Mensagem \_ SETBUTTONTEXT do PSM

Define o texto em um botão em um assistente do Aero. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ PropSheet SetButtonText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um dos valores a seguir especificando o botão cujo texto está definido.



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

O texto a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





