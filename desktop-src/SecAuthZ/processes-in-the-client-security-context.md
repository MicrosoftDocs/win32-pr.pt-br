---
description: Um aplicativo de servidor pode chamar a função CreateProcessAsUser para criar um novo processo que é executado em um contexto de segurança de clientes.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Processos no contexto do Client Security
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749963"
---
# <a name="processes-in-the-client-security-context"></a>Processos no contexto do Client Security

Um aplicativo de servidor pode chamar a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para criar um novo processo que é executado no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly)de um cliente. Quando chamado com o token de [*acesso*](/windows/desktop/SecGloss/a-gly)de um cliente, **CreateProcessAsUser** exige o \_ nome de ASSIGNPRIMARYTOKEN se \_ e se \_ aumentar os privilégios de nome de \_ cota \_ , que são mantidos pelos serviços do Windows em execução na [conta LocalSystem](/windows/desktop/Services/localsystem-account).

A função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) também requer um [*token de acesso primário*](/windows/desktop/SecGloss/p-gly). Um servidor pode obter um token de acesso primário para um cliente [iniciando uma sessão de logon](client-logon-sessions.md) para o cliente ou [representando o cliente](client-impersonation.md) e duplicando o token de [*representação*](/windows/desktop/SecGloss/i-gly).

Os procedimentos a seguir descrevem duas maneiras de criar um processo de cliente.

**Para criar um processo de cliente fazendo logon no cliente**

1.  Faça logon do cliente no computador local usando as [*credenciais*](/windows/desktop/SecGloss/c-gly) do cliente em uma chamada para [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** produz um token primário para a sessão de [*logon*](/windows/desktop/SecGloss/l-gly)do cliente.
2.  Se o servidor precisar usar o contexto de segurança do cliente, obtenha acesso ao arquivo executável para o [*processo*](/windows/desktop/SecGloss/p-gly) do cliente usando o token primário em uma chamada para a função [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
3.  Crie um processo no contexto de segurança do cliente usando o token primário em uma chamada para [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Um processo criado usando a técnica a seguir pode não ser capaz de acessar os recursos de rede, a menos que ele tenha as [*credenciais*](/windows/desktop/SecGloss/c-gly)do cliente.

 

**Para criar um processo de cliente representando o cliente**

1.  Inicie a representação usando uma função de representação, como [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient).
2.  Chame a função [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obter um token de representação que tenha o contexto de segurança do cliente.
3.  Chame a função [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) para converter o token de representação em um token primário.
4.  Use o token primário em uma chamada para a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para criar um processo no contexto de segurança do cliente.

Por padrão, o [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) cria o [*processo*](/windows/desktop/SecGloss/p-gly) do cliente em uma área de trabalho e estação de janela não interativa. Para criar um processo interativo, o servidor deve primeiro definir as DACLs ( [*listas de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) da estação de janela interativa e da área de trabalho para garantir que o cliente tenha permissão para acessá-las. A maneira preferida de fazer isso é registrar o cliente em log, [obter o Sid (identificador de segurança) da sessão de logon do cliente](/previous-versions//aa446670(v=vs.85))e, em seguida, usar esse SID nas ACEs permitidas pelo Access na estação de janela interativa e na área de trabalho. O servidor pode então chamar **CreateProcessAsUser**, especificando a estação de janela interativa e a área de trabalho winsta0 \\ padrão. Para obter um exemplo que mostra esse procedimento, consulte [iniciando um processo interativo de cliente em C++](/previous-versions//aa379608(v=vs.85)).

 

 
