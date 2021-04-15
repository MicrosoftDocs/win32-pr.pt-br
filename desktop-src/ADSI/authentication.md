---
title: Autenticação (ADSI)
description: No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI de autenticação
- ADSI, usando, autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104453854"
---
# <a name="authentication-adsi"></a>Autenticação (ADSI)

No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório. A função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa as credenciais do thread de chamada para autenticação. A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) podem ser usados para especificar as credenciais que não sejam as do thread de chamada. Quando um objeto está associado a um usuário autenticado, o usuário tem permissão para acessar o objeto com suporte dos requisitos de segurança do serviço de diretório subjacente.

> [!Note]  
> A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) não devem ser usados para validar as credenciais do usuário. Para obter mais informações sobre como validar as credenciais do usuário, consulte o artigo 180548 da base de dados de conhecimento Microsoft, como [validar as credenciais do usuário em sistemas operacionais da Microsoft](https://support.microsoft.com/kb/180548).

 

O exemplo de código a seguir mostra como usar o método [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para autenticar um usuário.


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



 

 




