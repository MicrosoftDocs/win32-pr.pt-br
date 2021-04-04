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
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="41c2b-104">Configurando Visual Basic 6,0 para o desenvolvimento de ADSI</span><span class="sxs-lookup"><span data-stu-id="41c2b-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="41c2b-105">**Configurando o ambiente de desenvolvimento Microsoft Visual Studio 2010 para Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="41c2b-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="41c2b-106">Inicie o Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="41c2b-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="41c2b-107">Crie um novo projeto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="41c2b-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="41c2b-108">Adicione uma referência à **biblioteca de tipos do DS ativo**.</span><span class="sxs-lookup"><span data-stu-id="41c2b-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="41c2b-109">Se você não precisar de associação de objeto COM inicial, ignore esta etapa.</span><span class="sxs-lookup"><span data-stu-id="41c2b-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="41c2b-110">Selecione **projeto \| Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="41c2b-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="41c2b-111">Selecione a guia **com** .</span><span class="sxs-lookup"><span data-stu-id="41c2b-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="41c2b-112">Selecione **biblioteca de tipos active DS**.</span><span class="sxs-lookup"><span data-stu-id="41c2b-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="41c2b-113">Comece a programar com ADSI.</span><span class="sxs-lookup"><span data-stu-id="41c2b-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="41c2b-114">Antes de começar, faça logon em um domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="41c2b-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="41c2b-115">Você deve ter permissão para modificar o banco de dados Active Directory.</span><span class="sxs-lookup"><span data-stu-id="41c2b-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="41c2b-116">Por padrão, o administrador tem esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="41c2b-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="41c2b-117">**Um aplicativo de exemplo Visual Basic 6,0: modificando FullName e Description para um usuário**</span><span class="sxs-lookup"><span data-stu-id="41c2b-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="41c2b-118">Siga as etapas anteriores para criar um projeto de Visual Basic executável padrão.</span><span class="sxs-lookup"><span data-stu-id="41c2b-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="41c2b-119">Clique duas vezes no formulário.</span><span class="sxs-lookup"><span data-stu-id="41c2b-119">Double-click the Form.</span></span> <span data-ttu-id="41c2b-120">Em carregamento de formulário \_ , digite o seguinte.</span><span class="sxs-lookup"><span data-stu-id="41c2b-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="41c2b-121">Você deve substituir a cadeia de caracteres "LDAP:Binding = jeffsmith, CN = Users, DC = Fabrikam, DC = com" pelo ADsPath de um usuário existente em um contêiner em seu domínio.</span><span class="sxs-lookup"><span data-stu-id="41c2b-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="41c2b-122">Crie uma conta de usuário de teste que possa ser modificada para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="41c2b-122">Create a test user account that can be modified for this purpose.</span></span>
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

    

3.  <span data-ttu-id="41c2b-123">Pressione **<F5>** para executar o programa.</span><span class="sxs-lookup"><span data-stu-id="41c2b-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="41c2b-124">Para verificar as alterações, use a ferramenta de gerenciamento Active Directory usuários e computadores.</span><span class="sxs-lookup"><span data-stu-id="41c2b-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="41c2b-125">Para obter mais informações sobre como usar o ADSI e o Visual Basic, consulte [Acessando Active Directory usando o Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="41c2b-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




