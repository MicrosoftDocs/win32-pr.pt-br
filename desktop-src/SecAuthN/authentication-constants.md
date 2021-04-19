---
description: Lista as constantes usadas para APIs de autenticação da Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Constantes de autenticação (autenticação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748468"
---
# <a name="authentication-constants-authentication"></a>Constantes de autenticação (autenticação)

## <a name="credentials-management-constants"></a>Constantes de gerenciamento de credenciais

O gerenciamento de credenciais usa as seguintes constantes para especificar tamanhos máximos de cadeia de caracteres.



| Constante                                        | Descrição                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \_comprimento máximo da \_ mensagem \_ CREDUI<br/>         | Número máximo de caracteres para o membro **pszMessageText** de uma estrutura de [**\_ informações de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| CREDUI \_ tamanho máximo da \_ legenda \_<br/>         | Número máximo de caracteres para o membro **pszCaptionText** de uma estrutura de [**\_ informações de CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| \_comprimento de \_ \_ destino genérico CREDUI máximo \_<br/> | Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de destino.<br/>                                             |
| \_comprimento máximo \_ de \_ destino de domínio \_ CREDUI<br/>  | Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de domínio.<br/>                                             |
| CREDUI \_ tamanho máximo do \_ nome de usuário \_<br/>        | Número máximo de caracteres em uma cadeia de caracteres que especifica um nome de conta de usuário.<br/>                                       |
| \_comprimento máximo da \_ senha \_ do CREDUI<br/>        | Número máximo de caracteres em uma cadeia de caracteres que especifica uma senha.<br/>                                                |



 

## <a name="gina-defined-values"></a>Valores definidos da Gina

As funções de interface [*Gina*](/windows/desktop/SecGloss/g-gly) e de suporte do [*Winlogon*](/windows/desktop/SecGloss/w-gly) usam os valores definidos a seguir.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 



| Valor                                                              | Descrição                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**opção de logon do WLX \_ \_ \_ xxx**](wlx-logon-option-xxx.md)<br/> | Contém opções de logon predefinidas. Ele é usado pelo parâmetro *dwOptions* de [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).<br/> |
| [**WLX \_ SAS \_ Type \_ xxx**](wlx-sas-type-xxx.md)<br/>         | Define um tipo SAS específico.<br/>                                                                                              |



 

 

