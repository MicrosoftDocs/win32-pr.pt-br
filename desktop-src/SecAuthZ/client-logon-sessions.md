---
description: Um servidor com o privilégio ES TCB NAME, como um serviço Windows em execução na Conta localSystem, pode chamar a função \_ LogonUser para autenticar um cliente no computador em que o servidor está \_ sendo executado.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sessões de logon do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783018"
---
# <a name="client-logon-sessions"></a>Sessões de logon do cliente

Um servidor com o privilégio ES TCB NAME, como um serviço Windows em execução na Conta localSystem , pode chamar a função \_ \_ [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) [](/windows/desktop/Services/localsystem-account) [](/windows/desktop/SecGloss/a-gly) para autenticar um cliente no computador em que o servidor está sendo executado. A **função LogonUser** inicia uma nova sessão de [*logon*](/windows/desktop/SecGloss/s-gly) e retorna um [*token*](/windows/desktop/SecGloss/p-gly) de acesso primário que contém as informações de segurança do cliente. Você pode usar esse token primário ao chamar a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para representar o cliente ou chamar [](/windows/desktop/SecGloss/s-gly) a [**função CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para criar um processo executado no contexto de segurança do cliente.

[*A*](/windows/desktop/SecGloss/p-gly) vantagem de autenticar o cliente dessa maneira é que o servidor que representa o cliente autenticado ou um processo criado no contexto do cliente autenticado pode se conectar aos recursos de rede remota como o cliente. Se essa autenticação não for feita, o servidor poderá se conectar aos recursos de rede somente se tiver adquirido o nome da conta e a senha do cliente para passar para a [**função WNetAddConnection2.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)

A desvantagem de autenticar o cliente dessa maneira é que o servidor deve ter adquirido as credenciais do cliente [*(nome*](/windows/desktop/SecGloss/c-gly) de domínio, nome de usuário e senha). Se um cliente remoto fornece essas credenciais ao servidor, é responsabilidade do cliente e do servidor garantir que as credenciais sejam transmitidas de maneira segura.

 

 
