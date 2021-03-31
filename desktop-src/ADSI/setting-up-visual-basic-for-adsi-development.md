---
title: Configurando Visual Basic 6,0 para o desenvolvimento de ADSI
description: Este tópico discute como configurar Visual Basic no Visual Studio para desenvolver um aplicativo ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configurando Visual Basic para ADSI de desenvolvimento ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822183"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configurando Visual Basic 6,0 para o desenvolvimento de ADSI

**Configurando o ambiente de desenvolvimento Microsoft Visual Studio 2010 para Visual Basic**

1.  Inicie o Visual Studio 2010.
2.  Crie um novo projeto Visual Basic.
3.  Adicione uma referência à **biblioteca de tipos do DS ativo**.
    > [!Note]  
    > Se você não precisar de associação de objeto COM inicial, ignore esta etapa.

     

    1.  Selecione **projeto \| Adicionar referência**.
    2.  Selecione a guia **com** .
    3.  Selecione **biblioteca de tipos active DS**.

4.  Comece a programar com ADSI.

Antes de começar, faça logon em um domínio do Windows. Você deve ter permissão para modificar o banco de dados Active Directory. Por padrão, o administrador tem esse privilégio.

**Um aplicativo de exemplo Visual Basic 6,0: modificando FullName e Description para um usuário**

1.  Siga as etapas anteriores para criar um projeto de Visual Basic executável padrão.
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

    

3.  Pressione **<F5>** para executar o programa.
4.  Para verificar as alterações, use a ferramenta de gerenciamento Active Directory usuários e computadores. Para obter mais informações sobre como usar o ADSI e o Visual Basic, consulte [Acessando Active Directory usando o Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




