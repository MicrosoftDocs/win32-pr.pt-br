---
title: configurando Visual Basic 6,0 para o desenvolvimento de ADSI
description: este tópico discute como configurar Visual Basic no Visual Studio para desenvolver um aplicativo ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- configurando Visual Basic para adsi de desenvolvimento adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cadc9f74410dcb654a880920a83c20e6af9db1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885209"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>configurando Visual Basic 6,0 para o desenvolvimento de ADSI

**configurando o ambiente de desenvolvimento Microsoft Visual Studio 2010 para Visual Basic**

1.  Inicie o Visual Studio 2010.
2.  crie um novo projeto Visual Basic.
3.  Adicione uma referência à **biblioteca de tipos do DS ativo**.
    > [!Note]  
    > Se você não precisar de associação de objeto COM inicial, ignore esta etapa.

     

    1.  selecione **Project \| adicionar referência**.
    2.  Selecione a guia **com** .
    3.  Selecione **biblioteca de tipos active DS**.

4.  Comece a programar com ADSI.

antes de começar, faça logon em um domínio Windows. Você deve ter permissão para modificar o banco de dados Active Directory. Por padrão, o administrador tem esse privilégio.

**um aplicativo de exemplo Visual Basic 6,0: modificando FullName e Description para um usuário**

1.  siga as etapas anteriores para criar um projeto de Visual Basic executável padrão.
2.  Clique duas vezes no formulário. Em carregamento de formulário \_ , digite o seguinte. Você deve substituir a cadeia de caracteres "LDAP:Binding = jeffsmith, CN = Users, DC = Fabrikam, DC = com" pelo ADsPath de um usuário existente em um contêiner em seu domínio. Crie uma conta de usuário de teste que possa ser modificada para essa finalidade.
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

    

3.  Pressione **&lt; F5 &gt;** para executar o programa.
4.  Para verificar as alterações, use a ferramenta de gerenciamento Active Directory usuários e computadores. para obter mais informações sobre como usar o ADSI e o Visual Basic, consulte [acessando Active Directory usando o Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




