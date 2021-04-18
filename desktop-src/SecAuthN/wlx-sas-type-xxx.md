---
description: Os valores definem um tipo SAS específico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749683"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ Type \_ xxx

\[A \_ constante do tipo WLX SAS \_ \_ xxx não está mais disponível para uso a partir do Windows Server 2008 e do Windows Vista.\]

Os **valores \_ \_ \_ xxx do tipo SAS do WLX** definem um tipo SAS específico.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Todos os valores de zero a 127 são reservados para tipos definidos pela Microsoft. Os valores acima de 127 estão disponíveis para tipos definidos pelo cliente. Os tipos a seguir são passados para funções que têm um parâmetro *dwSasType* .



| Constante                                                                                                                                                                                                         | Descrição                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**\_tipo de SAS WLX \_ \_ Ctrl \_ ALT \_ del**</dt> </dl>            | Indica que um usuário digitou a SAS CTRL + ALT + DEL padrão.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ tipo \_ sc \_ Insert**</dt> </dl>                      | Indica que um [*cartão inteligente*](../secgloss/s-gly.md) foi inserido em um dispositivo compatível.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ tipo \_ sc \_ Remove**</dt> </dl>                      | Indica que um cartão inteligente foi removido de um dispositivo compatível.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**\_ \_ atividade SCRNSVR do tipo SAS \_ do \_ WLX**</dt> </dl> | Indica que a atividade do teclado ou do mouse ocorreu enquanto uma proteção de tela segura estava ativa.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout**</dt> </dl>    | Indica que a ativação da proteção de tela ocorreu devido à inatividade do teclado e do mouse.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**\_ \_ tempo limite de tipo SAS WLX \_**</dt> </dl>                             | Indica que nenhuma entrada de usuário foi recebida dentro do período de tempo limite especificado.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**\_logoff do \_ usuário do tipo SAS \_ WLX \_**</dt> </dl>                | Indica que o usuário está sendo desconectado do sistema.<br/>                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 
