---
title: Autenticação (ADSI)
description: No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI de autenticação
- ADSI, Usando, Autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840553"
---
# <a name="authentication-adsi"></a>Autenticação (ADSI)

No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório. A [**função ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa as credenciais do thread de chamada para autenticação. A [**função ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) podem ser usados para especificar credenciais diferentes daquelas do thread de chamada. Quando um objeto é vinculado a com um usuário autenticado, o usuário tem permissão para acessar o objeto conforme suportado pelos requisitos de segurança do serviço de diretório subjacente.

> [!Note]  
> A [**função ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) não devem ser usados para validar as credenciais do usuário. Para obter mais informações sobre como validar credenciais de usuário, consulte Base de Dados de Conhecimento Microsoft artigo 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).

 

O exemplo de código a seguir mostra como usar o [**método OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para autenticar um usuário.


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




