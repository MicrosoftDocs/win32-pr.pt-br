---
description: Um servidor com o privilégio de nome do SE \_ TCB \_ , como um serviço do Windows em execução na conta LocalSystem, pode chamar a função LogonUser para autenticar um cliente no computador em que o servidor está sendo executado.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sessões de logon do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1439b27637b0e46df3b468b42cb9c45ac8f759f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502185"
---
# <a name="client-logon-sessions"></a>Sessões de logon do cliente

Um servidor com o privilégio de nome do SE \_ TCB \_ , como um serviço do Windows em execução na [conta LocalSystem](/windows/desktop/Services/localsystem-account), pode chamar a função [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) para [*autenticar*](/windows/desktop/SecGloss/a-gly) um cliente no computador em que o servidor está sendo executado. A função **LogonUser** inicia uma nova [*sessão*](/windows/desktop/SecGloss/s-gly) de logon e retorna um [*token de acesso primário*](/windows/desktop/SecGloss/p-gly) que contém as informações de segurança do cliente. Você pode usar esse token primário ao chamar a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) para representar o cliente ou chamar a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para criar um processo que é executado no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do cliente.

A vantagem de autenticar o cliente dessa forma é que o servidor que representa o cliente autenticado ou um [*processo*](/windows/desktop/SecGloss/p-gly) criado no contexto do cliente autenticado pode se conectar a recursos de rede remota como o cliente. Se essa autenticação não for feita, o servidor poderá se conectar a recursos de rede somente se tiver adquirido o nome da conta e a senha do cliente para passar para a função [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .

A desvantagem de autenticar o cliente dessa forma é que o servidor deve ter adquirido as [*credenciais*](/windows/desktop/SecGloss/c-gly) do cliente (nome de domínio, nome de usuário e senha). Se um cliente remoto fornecer essas credenciais ao servidor, é responsabilidade do cliente e do servidor garantir que as credenciais sejam transmitidas de maneira segura.

 

 
