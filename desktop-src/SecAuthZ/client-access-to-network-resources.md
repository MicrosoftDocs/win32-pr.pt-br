---
description: Explica estratégias para acessar recursos de rede.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Acesso de cliente aos recursos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8886f474876080703d190efb3419d099027f24af17dd735736957452318e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783072"
---
# <a name="client-access-to-network-resources"></a>Acesso de cliente aos recursos de rede

Um servidor pode usar as seguintes estratégias para acessar os recursos de rede:

-   Se o servidor tiver o nome da conta e a senha de um cliente, ele poderá chamar [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) com as [*credenciais*](/windows/desktop/SecGloss/c-gly) do cliente para mapear uma letra da unidade local para um compartilhamento de rede.
-   Depois de chamar [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) com as credenciais do cliente, o servidor pode chamar a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) para [criar um processo para o cliente](processes-in-the-client-security-context.md). Esse novo processo de cliente pode acessar recursos de rede usando o [*contexto de segurança*](/windows/desktop/SecGloss/s-gly)do cliente. Por exemplo, o processo pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um arquivo em um computador remoto. O sistema usa o [*token principal*](/windows/desktop/SecGloss/p-gly) do cliente para verificar as tentativas de acesso pelo processo do cliente.
-   Um servidor pode chamar [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) com credenciais nulas para estabelecer uma conexão com um recurso de rede com acesso ao servidor ou uma conexão padrão. Se o servidor estiver sendo executado como a conta LocalSystem, ele se autenticará no recurso de rede no [*contexto de segurança*](/windows/desktop/SecGloss/s-gly) do servidor de domínio. Se o servidor estiver sendo executado em uma conta de serviço, ele será autenticado como essa conta. Para obter mais informações, consulte a [conta LocalSystem](/windows/desktop/Services/localsystem-account).

Para obter informações sobre como proteger senhas, consulte [manipulando senhas](/windows/desktop/SecBP/handling-passwords). Para obter informações sobre como adquirir credenciais, consulte [solicitando credenciais ao usuário](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
