---
description: Se você usar a API de script para o WMI, poderá definir privilégios de segurança específicos.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Executando operações privilegiadas usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091784"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Executando operações privilegiadas usando o VBScript

Se você usar a API de script para o WMI, poderá definir privilégios de segurança específicos. Por exemplo, você pode definir os privilégios de segurança para solicitar um desligamento do sistema operacional ou para examinar o log de eventos de segurança. Para obter mais informações, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

Você só precisa definir privilégios quando estiver acessando o WMI em seu computador. Quando você está acessando um host remoto, o COM RPC define automaticamente os privilégios. Para determinar todos os privilégios necessários, consulte a documentação para as classes específicas do WMI que você deseja acessar, como o [**sistema \_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem). Para obter mais informações, consulte [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

As seções a seguir são discutidas neste tópico:

-   [Definindo um privilégio do objeto de segurança \_](/windows)
-   [Definindo um privilégio como parte de um moniker](#setting-a-privilege-as-part-of-a-moniker)
-   [Revogando e redefinindo privilégios](#revoking-and-resetting-privileges)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Definindo um privilégio do objeto de segurança \_

Use o procedimento a seguir para definir privilégios de segurança em Visual Basic.

**Para definir privilégios em Visual Basic**

1.  Crie um objeto do tipo [**SWbemLocator**](swbemlocator.md).
2.  Adicione o novo privilégio ao objeto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .

    O objeto de [**segurança \_**](swbemlocator-security-.md) contém uma coleção [**SWbemObjectSet**](swbemobjectset.md) . Os objetos no conjunto são objetos [**SWbemSecurity**](swbemsecurity.md) . Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

3.  Faça logon no WMI e recupere um objeto [**SWbemServices**](swbemservices.md) .

    O objeto [**SWbemServices**](swbemservices.md) herda o privilégio que é definido na etapa anterior.

Você também pode definir um privilégio usando o método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Definindo um privilégio como parte de um moniker

Você pode definir um privilégio como parte de um moniker.

O exemplo a seguir mostra como adicionar um privilégio de depuração a um moniker.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Revogando e redefinindo privilégios

O exemplo a seguir mostra como definir o privilégio **SeDebugPrivilege** e revogar o privilégio **SeRemoteShutdownPrivilege** .


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> </dl>

 

 
