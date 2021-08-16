---
title: Propriedades de usuário personalizadas do WinNT
description: O provedor WinNT disponibiliza as propriedades personalizadas a seguir para a classe User. Eles podem ser acessados por meio dos métodos IADs.Get e IADs.Put. Para obter mais informações, consulte a estrutura USER \_ INFO \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- ADSI de propriedades personalizadas do usuário do WinNT
- ADSI do provedor WinNT, objeto de usuário, propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e12fc58ff4829f425302c1d13997f2e6c085646b1ace2c3e8ae2ebfb7df6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838385"
---
# <a name="winnt-custom-user-properties"></a>Propriedades de usuário personalizadas do WinNT

O provedor WinNT disponibiliza as propriedades personalizadas a seguir para a classe User. Eles podem ser acessados por meio [**dos métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) Para obter mais informações, consulte a [**estrutura USER \_ INFO \_ 3.**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3)



| Propriedade            | Tipo         | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Home Directory Drive do usuário. Este é um ponteiro para uma cadeia de caracteres Unicode que especifica o caminho do diretório home. A cadeia de caracteres pode ser **nula.** Consulte o exemplo neste tópico.                                                                                                                                                                                 |
| **Objectsid**       | Cadeia de caracteres de octeto | SID de objeto do usuário. Para obter um exemplo de como recuperar o SID de objeto usando o provedor WinNT, consulte SID de objeto [(provedor WinNT)](object-sid.md)                                                                                                                                                                                                          |
| **Parâmetros**      | String       | Parâmetros do usuário. Aponta para uma cadeia de caracteres Unicode que é reservado para uso por aplicativos. Essa cadeia de caracteres pode ser uma cadeia de caracteres nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação. Os produtos da Microsoft usam esse membro para armazenar dados de configuração do usuário. Essa propriedade só pode ser modificada por um aplicativo durante a instalação. |
| **PasswordAge**     | Tempo         | Duração do tempo da senha em uso. Essa propriedade indica o número de segundos decorridos desde que a senha foi alterada pela última vez.                                                                                                                                                                                                                    |
| **PasswordExpired** | Integer      | Informa quando a senha expirou. Quando você usar Get, ele retornará zero se a senha não tiver expirado ou se tiver expirado. Consulte o exemplo neste tópico.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Integer      | ID do grupo primário do usuário, por exemplo, ID do grupo de usuários do domínio. Consulte o exemplo neste tópico.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Integer      | Sinalizador de usuário definido em [**ADS \_ USER FLAG \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) Para ver um exemplo de como usar UserFlags, consulte [Password Never Expires (Provedor WinNT)](winnt-password-never-expires.md)                                                                                                                                                             |



 

Este exemplo mostra como definir o Diretório home drive de um usuário.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



Este exemplo mostra como usar PasswordExpired para forçar um usuário a alterar a senha no próximo logon.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



Este exemplo mostra como obter o grupo primário do usuário.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 