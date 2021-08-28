---
title: SBM_ENABLE_ARROWS mensagem (Winuser.h)
description: Um aplicativo envia a mensagem SBM ENABLE ARROWS para habilitar ou desabilitar uma ou \_ \_ ambas as setas de um controle de barra de rolagem.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- SBM_ENABLE_ARROWS controles de Windows mensagem
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e7f3ef8728befe72ec4f2c4afe39caeb10bc0b58984612a5db2445963dc549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770016"
---
# <a name="sbm_enable_arrows-message"></a>Mensagem \_ HABILITAR SETAS do SBM \_

Um aplicativo envia a **mensagem SBM \_ ENABLE \_ ARROWS** para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se as setas da barra de rolagem estão habilitadas ou desabilitadas e indica quais setas estão habilitadas ou desabilitadas. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                   | Significado                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ DISABLE \_ BOTH**</dt> </dl> | Desabilita as duas setas em uma barra de rolagem.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**DESABILITAÇÃO DE ESB \_ \_ PARA BAIXO**</dt> </dl> | Desabilita a seta para baixo em uma barra de rolagem vertical.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**ESB \_ DISABLE \_ LTUP**</dt> </dl> | Desabilita a seta para a esquerda em uma barra de rolagem horizontal ou a seta para cima em uma barra de rolagem vertical.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**ESB \_ DISABLE \_ LEFT**</dt> </dl> | Desabilita a seta para a esquerda em uma barra de rolagem horizontal.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**ESB \_ DISABLE \_ RTDN**</dt> </dl> | Desabilita a seta para a direita em uma barra de rolagem horizontal ou a seta para baixo em uma barra de rolagem vertical.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**ESB \_ DISABLE \_ UP**</dt> </dl>       | Desabilita a seta para cima em uma barra de rolagem vertical.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**ESB \_ ENABLE \_ BOTH**</dt> </dl>    | Habilita as duas setas em uma barra de rolagem.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será **TRUE;** caso contrário, será **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





