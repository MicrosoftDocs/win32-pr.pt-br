---
description: Active Directory objetos podem ser usados para localizar recursos em um domínio de rede de computador, como usuários, políticas de segurança, impressoras, componentes distribuídos e outros recursos.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Criando e atualizando objetos Active Directory
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814141"
---
# <a name="creating-and-updating-active-directory-objects"></a>Criando e atualizando objetos Active Directory

Active Directory objetos podem ser usados para localizar recursos em um domínio de rede de computador, como usuários, políticas de segurança, impressoras, componentes distribuídos e outros recursos. Active Directory objetos podem ser criados e atualizados usando o WMI. Você pode atualizar um objeto Active Directory quando novas informações sobre o objeto se tornarem disponíveis usando a notificação de eventos do WMI. Por exemplo, quando um objeto de usuário Active Directory é criado, você pode detectar sua criação com uma consulta de evento no WMI e, quando o evento é recebido, você pode atualizar o objeto com novas informações.

O exemplo de código a seguir cria uma nova instância de WMI da classe que representa o objeto de usuário Active Directory. O exemplo mostra como atribuir valores a várias propriedades necessárias para criar a nova instância de usuário Active Directory.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



O exemplo de código a seguir atualiza uma instância WMI de um objeto Active Directory. Neste exemplo, o atributo DisplayName é atualizado.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



