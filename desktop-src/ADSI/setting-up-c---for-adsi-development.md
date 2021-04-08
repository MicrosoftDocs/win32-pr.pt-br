---
title: Configurando Visual C++ 6,0 para o desenvolvimento de ADSI
description: Este tópico mostra como configurar o C++ no Visual Studio para que você possa desenvolver um aplicativo ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configurando C++ para o desenvolvimento de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004858"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a><span data-ttu-id="5b4af-104">Configurando Visual C++ 6,0 para o desenvolvimento de ADSI</span><span class="sxs-lookup"><span data-stu-id="5b4af-104">Setting Up Visual C++ 6.0 for ADSI Development</span></span>

<span data-ttu-id="5b4af-105">O sistema de desenvolvimento Microsoft Visual C++ 6,0 pode ser usado para desenvolver aplicativos empresariais.</span><span class="sxs-lookup"><span data-stu-id="5b4af-105">The Microsoft Visual C++ 6.0 development system can be used to develop enterprise applications.</span></span> <span data-ttu-id="5b4af-106">Para configurar seu ambiente Visual C++ 6,0 para desenvolver um aplicativo ADSI, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="5b4af-106">To set up your Visual C++ 6.0 environment to develop an ADSI application, perform the following steps:</span></span>

<span data-ttu-id="5b4af-107">**Configurando o ambiente de desenvolvimento Microsoft Visual C++ 6,0**</span><span class="sxs-lookup"><span data-stu-id="5b4af-107">**Setting Up the Microsoft Visual C++ 6.0 Development Environment**</span></span>

1.  <span data-ttu-id="5b4af-108">Aponte para o diretório de inclusão e biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5b4af-108">Point to the include and library directory.</span></span> <span data-ttu-id="5b4af-109">Selecione **ferramentas \| Opções**.</span><span class="sxs-lookup"><span data-stu-id="5b4af-109">Select **Tools \| Options**.</span></span> <span data-ttu-id="5b4af-110">Clique na guia **diretório** e especifique o caminho para os arquivos de cabeçalho ADSI.</span><span class="sxs-lookup"><span data-stu-id="5b4af-110">Click the **Directory** tab, and specify the path to the ADSI header files.</span></span>
2.  <span data-ttu-id="5b4af-111">Inclua o arquivo activeds. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="5b4af-111">Include the Activeds.h file in your project.</span></span>
3.  <span data-ttu-id="5b4af-112">Adicione os arquivos activeds. lib e adsiid. lib à entrada do vinculador para o seu projeto.</span><span class="sxs-lookup"><span data-stu-id="5b4af-112">Add the Activeds.lib and Adsiid.lib files to the linker input for your project.</span></span>
4.  <span data-ttu-id="5b4af-113">Comece a programar com ADSI.</span><span class="sxs-lookup"><span data-stu-id="5b4af-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="5b4af-114">Faça logon em um domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b4af-114">Log on to a Windows domain.</span></span> <span data-ttu-id="5b4af-115">Você também deve ter permissão para modificar dados em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5b4af-115">You must also have permission to modify data in Active Directory.</span></span> <span data-ttu-id="5b4af-116">Por padrão, o administrador tem esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="5b4af-116">By default, the Administrator has this privilege.</span></span> <span data-ttu-id="5b4af-117">Para inserir este exemplo de código:</span><span class="sxs-lookup"><span data-stu-id="5b4af-117">To enter this code example:</span></span>

<span data-ttu-id="5b4af-118">**Um aplicativo de Visual C++ de exemplo: Criando um usuário em um domínio**</span><span class="sxs-lookup"><span data-stu-id="5b4af-118">**A Sample Visual C++ Application: Creating a User in a Domain**</span></span>

1.  <span data-ttu-id="5b4af-119">Inicie o Visual C++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="5b4af-119">Start Visual C++ 6.0.</span></span>
2.  <span data-ttu-id="5b4af-120">Crie um projeto executável autônomo.</span><span class="sxs-lookup"><span data-stu-id="5b4af-120">Create a standalone executable project.</span></span> <span data-ttu-id="5b4af-121">Pode ser um aplicativo MFC, ATL ou console.</span><span class="sxs-lookup"><span data-stu-id="5b4af-121">It can be either an MFC, ATL, or Console Application.</span></span>
3.  <span data-ttu-id="5b4af-122">Siga as etapas anteriores para configurar seu projeto.</span><span class="sxs-lookup"><span data-stu-id="5b4af-122">Follow the previous steps to set up your project.</span></span>
4.  <span data-ttu-id="5b4af-123">Insira o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b4af-123">Enter the following code example.</span></span> <span data-ttu-id="5b4af-124">Substitua a cadeia de caracteres "LDAP:Binding = Users, DC = Fabrikam, DC = com" pelo ADsPath de um contêiner em seu domínio.</span><span class="sxs-lookup"><span data-stu-id="5b4af-124">Replace the "LDAP://CN=users,DC=fabrikam,DC=com" string with the ADsPath of a container in your domain.</span></span> <span data-ttu-id="5b4af-125">Você também deve substituir o nome de usuário "jeffsmith" por um nome de usuário que seja exclusivo em seu domínio.</span><span class="sxs-lookup"><span data-stu-id="5b4af-125">You should also replace the user name "jeffsmith" with a user name that is unique in your domain.</span></span>

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  <span data-ttu-id="5b4af-126">Crie e execute o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5b4af-126">Build and run the application.</span></span> <span data-ttu-id="5b4af-127">Para verificar se o usuário foi criado, use a ferramenta de gerenciamento Active Directory usuários e computadores.</span><span class="sxs-lookup"><span data-stu-id="5b4af-127">To verify that the user has been created, use the Active Directory Users and Computers management tool.</span></span>

 

 




