---
title: Obtendo dados do computador local
description: Embora Gerenciamento Remoto do Windows e WS-Management protocolo sejam explicitamente projetados para comunicação remota, o estabelecimento de uma sessão no computador local é o caso mais simples.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641126"
---
# <a name="obtaining-data-from-the-local-computer"></a>Obtendo dados do computador local

Embora Gerenciamento Remoto do Windows e WS-Management protocolo sejam explicitamente projetados para comunicação remota, o estabelecimento de uma sessão no computador local é o caso mais simples. Alguns scripts podem exigir acesso aos dados no computador local, bem como em computadores remotos.

**WinRM versão 2,0:  **

Todas as operações são consideradas remotas e o serviço WinRM deve ser iniciado antes de qualquer operação ser executada. Se um destino remoto não for especificado, o localhost será usado por padrão e todas as operações serão enviadas para o serviço WinRM local. Para obter mais informações sobre como iniciar o serviço WinRM, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

Ao usar o serviço WinRM para operações locais, os seguintes fatores devem ser considerados:

-   A configuração local do WinRM só pode ser lida por administradores.
-   Os namespaces do WMI devem ter permissões de habilitação remota definidas. Para obter mais informações, consulte [protegendo uma conexão WMI remota](../wmisdk/securing-a-remote-wmi-connection.md).
-   Se um [*ouvinte*](windows-remote-management-glossary.md) do WinRM não for criado, o serviço WinRM escutará solicitações locais na porta 47001.

Cada script do WinRM deve começar estabelecendo uma sessão ou conexão com um computador criando um objeto de [**sessão**](session.md) . Depois que a sessão é criada, você pode usar os métodos de objeto de **sessão** , como [**Session. enumera**](session-enumerate.md) ou [**Session. Invoke**](session-invoke.md) para obter dados ou para executar métodos.

A criação de uma sessão é um pouco semelhante à [conexão](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) com um namespace Instrumentação de gerenciamento do Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page)). A sessão é essencialmente uma camada que permite que você envie e receba dados por meio de mensagens [*SOAP*](windows-remote-management-glossary.md) e do protocolo WS-Management. Para obter mais informações, consulte [protocolo WS-Management](ws-management-protocol.md).

Chamar o método [**WSMan. CreateSession**](wsman-createsession.md) para criar um objeto de [**sessão**](session.md) iniciará uma [*sessão*](windows-remote-management-glossary.md) que se conecta ao WinRM local.

**Para criar uma sessão do WSMan e obter dados**

1.  Crie um objeto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Crie uma sessão chamando o método [**WSMan. CreateSession**](wsman-createsession.md) . Essa sessão é executada sob seu nome de usuário e senha de logon e pode obter dados por meio do WinRM local.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Crie um [*URI*](windows-remote-management-glossary.md) de recurso para identificar o [*recurso*](windows-remote-management-glossary.md) que você deseja gerenciar ou para o qual deseja obter dados. Para obter mais informações sobre como formatar um URI, consulte [URIs de recurso](resource-uris.md). Esse URI de recurso é para uma instância específica da classe [**de \_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) , o serviço Winmgmt. Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Chamar métodos de [**sessão**](session.md) que obtêm ou enumeram dados usando o URI de recurso. Para obter mais informações, consulte [API de script do WinRM](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Para obter ou gerenciar dados de outro computador ou usar métodos diferentes de autenticação, consulte [obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md).

O exemplo de código VBScript a seguir mostra o script completo que obtém a instância específica do [**\_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) chamado "winmgmt".


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



O exemplo de código VBScript a seguir mostra o script completo com a transformação de dados. Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 