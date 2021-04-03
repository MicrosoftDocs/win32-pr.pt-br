---
title: Mensagem de SBM_ENABLE_ARROWS (WinUser. h)
description: Um aplicativo envia a mensagem de SBM \_ habilitar \_ setas para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Controles de SBM_ENABLE_ARROWS de mensagens do Windows
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
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918864"
---
# <a name="sbm_enable_arrows-message"></a>Mensagem de SBM \_ habilitar \_ setas

Um aplicativo envia a mensagem de **SBM \_ habilitar \_ setas** para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se as setas da barra de rolagem estão habilitadas ou desabilitadas e indica quais setas estão habilitadas ou desabilitadas. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                   | Significado                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <dt>**ESB \_ desabilita \_ ambos**</dt> </dl> | Desabilita ambas as setas em uma barra de rolagem.<br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <dt>**\_desabilitação do ESB \_**</dt> </dl> | Desabilita a seta para baixo em uma barra de rolagem vertical.<br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <dt>**\_LTUP de desabilitação de ESB \_**</dt> </dl> | Desabilita a seta para a esquerda em uma barra de rolagem horizontal ou na seta para cima em uma barra de rolagem vertical.<br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <dt>**\_desabilitação do ESB \_ restante**</dt> </dl> | Desabilita a seta para a esquerda em uma barra de rolagem horizontal.<br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <dt>**\_RTDN de desabilitação de ESB \_**</dt> </dl> | Desabilita a seta para a direita em uma barra de rolagem horizontal ou na seta para baixo em uma barra de rolagem vertical.<br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <dt>**\_desabilitação do ESB \_**</dt> </dl>       | Desabilita a seta para cima em uma barra de rolagem vertical.<br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <dt>**habilitado para ESB \_ \_**</dt> </dl>    | Habilita ambas as setas em uma barra de rolagem.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 





