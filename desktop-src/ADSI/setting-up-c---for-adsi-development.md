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
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Configurando Visual C++ 6,0 para o desenvolvimento de ADSI

O sistema de desenvolvimento Microsoft Visual C++ 6,0 pode ser usado para desenvolver aplicativos empresariais. Para configurar seu ambiente Visual C++ 6,0 para desenvolver um aplicativo ADSI, execute as seguintes etapas:

**Configurando o ambiente de desenvolvimento Microsoft Visual C++ 6,0**

1.  Aponte para o diretório de inclusão e biblioteca. Selecione **ferramentas \| Opções**. Clique na guia **diretório** e especifique o caminho para os arquivos de cabeçalho ADSI.
2.  Inclua o arquivo activeds. h em seu projeto.
3.  Adicione os arquivos activeds. lib e adsiid. lib à entrada do vinculador para o seu projeto.
4.  Comece a programar com ADSI.

Faça logon em um domínio do Windows. Você também deve ter permissão para modificar dados em Active Directory. Por padrão, o administrador tem esse privilégio. Para inserir este exemplo de código:

**Um aplicativo de Visual C++ de exemplo: Criando um usuário em um domínio**

1.  Inicie o Visual C++ 6,0.
2.  Crie um projeto executável autônomo. Pode ser um aplicativo MFC, ATL ou console.
3.  Siga as etapas anteriores para configurar seu projeto.
4.  Insira o exemplo de código a seguir. Substitua a cadeia de caracteres "LDAP:Binding = Users, DC = Fabrikam, DC = com" pelo ADsPath de um contêiner em seu domínio. Você também deve substituir o nome de usuário "jeffsmith" por um nome de usuário que seja exclusivo em seu domínio.

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

    

5.  Crie e execute o aplicativo. Para verificar se o usuário foi criado, use a ferramenta de gerenciamento Active Directory usuários e computadores.

 

 




