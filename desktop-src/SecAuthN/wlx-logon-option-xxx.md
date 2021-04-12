---
description: Os valores são usados pelo parâmetro dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297076"
---
# <a name="wlx_logon_option_xxx"></a>opção de logon do WLX \_ \_ \_ xxx

\[A \_ constante da opção de logon WLX \_ \_ xxx não está mais disponível para uso a partir do Windows Server 2008 e do Windows Vista.\]

Os valores da **\_ opção de logon WLX \_ \_ xxx** são usados pelo parâmetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Após um logon bem-sucedido, sua DLL GINA pode usar esse valor para especificar a opção a seguir.



| Constante                                                                                                                                                                                          | Descrição                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**\_ \_ \_ não aceitar \_ perfil de logon WLX**</dt> </dl> | Especifica que o Winlogon não deve carregar um perfil para o usuário conectado. Nesse caso, sua DLL GINA carregará o perfil ou o usuário não precisará de um perfil.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 




