---
title: Propriedades do usuário personalizado do WinNT
description: O provedor WinNT disponibiliza as seguintes propriedades personalizadas para a classe User. Eles podem ser acessados por meio dos métodos IADs. Get e IADs. put. Para obter mais informações, consulte a \_ estrutura User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- ADSI das propriedades do usuário personalizado do WinNT
- ADSI do provedor WinNT, objeto de usuário, propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917680"
---
# <a name="winnt-custom-user-properties"></a>Propriedades do usuário personalizado do WinNT

O provedor WinNT disponibiliza as seguintes propriedades personalizadas para a classe User. Eles podem ser acessados por meio dos métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . Para obter mais informações, consulte a estrutura [**user \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .



| Propriedade            | Type         | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Unidade do diretório base do usuário. Esse é um ponteiro para uma cadeia de caracteres Unicode que especifica o caminho do diretório base. A cadeia de caracteres pode ser **nula**. Consulte o exemplo neste tópico.                                                                                                                                                                                 |
| **ObjectSID**       | Cadeia de caracteres de octeto | SID de objeto do usuário. Para obter um exemplo de como recuperar o SID do objeto usando o provedor WinNT, consulte [SID do objeto (provedor winnt)](object-sid.md)                                                                                                                                                                                                          |
| **Parâmetros**      | String       | Parâmetros do usuário. Aponta para uma cadeia de caracteres Unicode que é reservada para uso por aplicativos. Essa cadeia de caracteres pode ser uma cadeia de caracteres nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação. Os produtos da Microsoft usam esse membro para armazenar dados de configuração do usuário. Essa propriedade só pode ser modificada por um aplicativo durante a instalação. |
| **Senha**     | Hora         | Duração de tempo da senha em uso. Essa propriedade indica o número de segundos decorridos desde que a senha foi alterada pela última vez.                                                                                                                                                                                                                    |
| **PasswordExpired** | Inteiro      | Informa quando a senha expirou. Quando você usa Get, ele retornará zero será a senha não expirou ou será diferente de zero se tiver expirado. Consulte o exemplo neste tópico.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Inteiro      | ID do grupo primário do usuário, por exemplo, ID do grupo de usuários de domínio. Consulte o exemplo neste tópico.                                                                                                                                                                                                                                                                        |
| **Sinalizadors de**       | Inteiro      | Sinalizador de usuário definido [**na \_ \_ \_ enumeração de sinalizador de usuário do ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Para obter um exemplo de como usar UserFlags, consulte a [senha nunca expira (provedor de winnt)](winnt-password-never-expires.md)                                                                                                                                                             |



 

Este exemplo mostra como definir o diretório da unidade inicial de um usuário.


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



 

 