---
description: Os valores são usados pelo parâmetro dwOptions de WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae482fa7af757a18fc3a38f809befbee94e4d59753cde8e35e01d172bcc065d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914755"
---
# <a name="wlx_logon_option_xxx"></a>OPÇÃO DE LOGON DO WLX \_ \_ \_ XXX

\[A constante WLX LOGON OPTION XXX não está mais disponível para uso no \_ \_ Windows Server \_ 2008 e Windows Vista.\]

Os **valores WLX \_ LOGON OPTION \_ \_ XXX** são usados pelo *parâmetro dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).

> [!Note]  
> As DLLs DE VALOR são ignoradas no Windows Vista.

 

Após um logon bem-sucedido, sua DLL DOIS pode usar esse valor para especificar a opção a seguir.



| Constante                                                                                                                                                                                          | Descrição                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**LOGON DO WLX \_ \_ NÃO OPT NO \_ \_ PROFILE**</dt> </dl> | Especifica que o Winlogon não deve carregar um perfil para o usuário conectado. Nesse caso, sua DLL DOEI carregará o perfil ou o usuário não precisará de um perfil.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 




