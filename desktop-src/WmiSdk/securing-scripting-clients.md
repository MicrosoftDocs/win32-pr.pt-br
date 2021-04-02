---
description: Scripts e Visual Basic aplicativos devem definir a segurança DCOM, especialmente para acesso remoto, e também podem precisar habilitar privilégios.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protegendo clientes de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165205"
---
# <a name="securing-scripting-clients"></a>Protegendo clientes de script

Scripts e Visual Basic aplicativos devem definir a segurança DCOM, especialmente para acesso remoto, e também podem precisar habilitar privilégios.

## <a name="default-access-permissions"></a>Permissões de acesso padrão

O acesso ao WMI é diferente entre computadores locais e remotos. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

A seguir estão as permissões de acesso padrão por conta:

-   Todos, LocalService, NetworkService

    Permissão para ler ou gravar dados e para executar [*métodos de provedor*](gloss-p.md) no computador local. Essas contas não podem criar novas classes ou instalar novos provedores.

-   Contas de administrador

    Controle total no computador local. Ao se conectar a um computador remoto, a conta deve ser um administrador local no computador remoto também.

## <a name="securing-a-scripting-client"></a>Protegendo um cliente de script

Os aplicativos de script e Visual Basic do WMI devem definir os níveis de segurança do DCOM adequadamente para os sistemas operacionais aos quais eles estão direcionados. Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

Ao se conectar a um computador remoto, talvez seja necessário alterar o serviço (NTLM ou Kerberos) que manipula a autenticação. Para obter mais informações, consulte [definindo o serviço de autenticação usando o VBScript](setting-the-authentication-service-using-vbscript.md).

O acesso a algumas classes ou dados WMI pode exigir um privilégio que não está habilitado. Por exemplo, você deve incluir o privilégio de segurança ao se conectar à classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) . Para obter mais informações, consulte [executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md).

Se você estiver acessando o WMI de uma página de Active Server (ASP), algumas configurações do IIS serão necessárias. Para obter mais informações, consulte [Configuring IIS 5,0 and posterior for WMI ASP scripting](configuring-iis-5-for-wmi-asp-scripting.md).

Você pode estar tentando se conectar a um namespace que requer uma conexão criptografada, em outras palavras, uma que exija um nível de autenticação de pktPrivacy. Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
