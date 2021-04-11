---
description: O formato de cadeia de caracteres do moniker é semelhante ao de um caminho de objeto WMI padrão. Para obter mais informações, consulte requisitos de caminho do objeto WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construindo uma cadeia de caracteres de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296636"
---
# <a name="constructing-a-moniker-string"></a>Construindo uma cadeia de caracteres de moniker

O formato de cadeia de caracteres do moniker é semelhante ao de um caminho de objeto WMI padrão. Para obter mais informações, consulte [requisitos de caminho do objeto WMI](wmi-object-path-requirements.md).

Um moniker tem as seguintes partes:

-   O prefixo WinMgmts: (obrigatório). O prefixo instrui o WSH (Windows Script Host) que o código a seguir usará os [objetos da API de script](scripting-api-objects.md).
-   Um componente de configurações de segurança (opcional)
-   Um componente de caminho do objeto WMI (opcional)

Você não pode especificar uma senha em uma cadeia de caracteres do moniker WMI. Se você precisar alterar a senha (parâmetro *strPassword* ) ou o tipo de autenticação (parâmetro *strAuthority* ) ao se conectar ao WMI, chame [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Lembre-se de que você só pode especificar a senha e a autoridade em conexões com computadores remotos. A tentativa de defini-los em um script em execução no computador local resulta em um erro. Para obter mais informações sobre quando as configurações de segurança e os componentes do caminho do objeto são usados, consulte [configurações de segurança do WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).

O moniker a seguir especifica o objeto [**SWbemServices**](swbemservices.md) que representa o padrão raiz do namespace \\ , com a representação on e o privilégio wbemPrivilegeDebug (SeDebugPrivilege) habilitado e o privilégio wbemPrivilegeSecurity (SeSecurityPrivilege) desabilitado.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Todas as literais de cadeia de caracteres não diferenciam maiúsculas de minúsculas.
>
> O prefixo "!" em um privilégio indica que o privilégio deve ser desabilitado; a omissão desse prefixo indica que o privilégio deve ser habilitado.
>
> O prefixo "!" é usado no nome do computador ou namespace quando as configurações de segurança são especificadas entre colchetes antes do nome do computador ou namespace.

 

As atribuições padrão a seguir são permitidas ao especificar o caminho do objeto:

-   O nome da máquina do computador pode ser omitido do caminho do objeto; nesse caso, o nome do computador local é assumido.
-   O namespace pode ser omitido do caminho do objeto; nesse caso, o namespace padrão é assumido.

    Isso é determinado pelo valor da chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting** \\ **padrão namespace**, o valor padrão é "root \\ CIMv2".

-   Uma classe ou instância também pode ser especificada; nesse caso, o objeto retornado é um objeto WMI em vez de um objeto de serviços.

> [!Note]  
> Se uma classe ou instância for especificada, você não poderá omitir o namespace ao especificar o nome da máquina do computador.

 

Para obter uma referência das constantes de privilégio usadas na cadeia de caracteres do moniker WMI, consulte [constantes de privilégio](privilege-constants.md)e os descritores de "nome curto de script".

## <a name="valid-moniker-strings"></a>Cadeias de caracteres de moniker válidas

Os exemplos a seguir mostram cadeias de caracteres de moniker válidas.

O moniker a seguir identifica o namespace padrão no computador local. Um objeto [**SWbemServices**](swbemservices.md) é retornado.


```VB
WinMgmts:
```



O moniker a seguir identifica o namespace padrão no computador meuservidor. Um objeto [**SWbemServices**](swbemservices.md) é retornado.


```VB
"WinMgmts://myServer"
```



O moniker a seguir identifica o \\ namespace raiz cimv2 no computador meuservidor. Um objeto [**SWbemServices**](swbemservices.md) é retornado.


```VB
"WinMgmts://myServer/root/cimv2"
```



O moniker a seguir identifica o \\ namespace raiz cimv2 no servidor local. Um objeto [**SWbemServices**](swbemservices.md) é retornado.


```VB
"WinMgmts:root/cimv2"
```



O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no \\ namespace raiz cimv2 no servidor meuservidor. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no \\ namespace raiz cimv2 no servidor local. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



O moniker a seguir identifica a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no namespace padrão no servidor local. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no namespace de script padrão no servidor local. Um objeto [**SWbemObject**](swbemobject.md) é retornado. O namespace padrão para scripts é determinado pela definição de configuração de namespace padrão, conforme especificado no controle WMI. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no \\ namespace raiz cimv2 no servidor meuservidor. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no \\ namespace raiz cimv2 no servidor local. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



O moniker a seguir identifica a instância [**do \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondente à unidade C: no namespace padrão no servidor local. Um objeto [**SWbemObject**](swbemobject.md) é retornado.


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



O moniker a seguir define o nível de representação para representar e define o \_ privilégio de depuração se.


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



O moniker a seguir define o nível de representação para representar e define o \_ privilégio de depuração se. Ele também revoga o privilégio de \_ desligamento se.


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



O moniker a seguir recupera descrições localizadas do inglês americano para a classe **MyClass** do \\ namespace WMI raiz.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



O moniker a seguir solicita a autenticação Kerberos usando o servidor principal mydomain \\ .


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



O moniker a seguir solicita a autenticação NTLM usando o domínio mydomain.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



O exemplo de código VBScript a seguir mostra como combinar parâmetros de segurança e localidade em um moniker.


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Embora os monikers forneçam acesso mais direto a objetos, em determinadas circunstâncias, o uso repetido de monikers pode ser menos eficiente do que o código equivalente que se conecta explicitamente ao WMI. Se o desempenho do aplicativo for uma consideração, considere usar os mecanismos alternativos.
>
> Não é possível usar a função **GetObject** fornecida pelo VBScript para atualizar ou definir dados ao executar scripts inseridos em uma página HTML, pois o Microsoft Internet Explorer nega o uso dessa chamada por motivos de segurança.

 

 

 
