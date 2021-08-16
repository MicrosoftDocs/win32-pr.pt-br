---
title: Configurando o Visual Basic 6.0 para desenvolvimento adsi
description: Este tópico discute como configurar o Visual Basic no Visual Studio para desenvolver um aplicativo ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configurando o Visual Basic adsi de desenvolvimento adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed2e0f4cd0b56ee0167deda2e998314bb313d1a98cd0c43a9f06b495a4324f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838676"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configurando o Visual Basic 6.0 para desenvolvimento adsi

**Configurando o ambiente de Microsoft Visual Studio 2010 para Visual Basic**

1.  Inicie o Visual Studio 2010.
2.  Crie um novo Visual Basic projeto.
3.  Adicione uma referência à **Biblioteca de Tipos active DS.**
    > [!Note]  
    > Se você não precisar de associação de objeto COM antecipada, ignore esta etapa.

     

    1.  Selecione **Project \| Adicionar Referência**.
    2.  Selecione a **guia COM.**
    3.  Selecione **Biblioteca de Tipos Active DS**.

4.  Comece a programar com ADSI.

Antes de começar, faça logoff em um Windows domínio. Você deve ter permissão para modificar o banco de dados do Active Directory. Por padrão, o Administrador tem esse privilégio.

**Um exemplo Visual Basic 6.0 Application: Modifying FullName and Description for a User**

1.  Siga as etapas anteriores para criar um projeto executável Visual Basic padrão.
2.  Clique duas vezes no Formulário. Em Carga \_ de Formulário, digite o seguinte. Você deve substituir a cadeia de caracteres "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" pelo ADsPath de um usuário existente em um contêiner em seu domínio. Crie uma conta de usuário de teste que possa ser modificada para essa finalidade.
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  Pressione **<F5>** para executar o programa.
4.  Para verificar as alterações, use a ferramenta Usuários e Computadores do Active Directory gerenciamento. Para obter mais informações sobre como usar a ADSI e Visual Basic, consulte [Acessando o Active Directory usando Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




