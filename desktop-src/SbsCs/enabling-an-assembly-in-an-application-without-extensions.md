---
description: Se o seu aplicativo não hospedar uma DLL, uma extensão, um plug-in ou um painel de controle, você poderá usar o método descrito nesta seção para habilitar um assembly para seu aplicativo.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Habilitando um assembly em um aplicativo sem extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142249"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Habilitando um assembly em um aplicativo sem extensões

Se o seu aplicativo não hospedar uma DLL, uma extensão, um plug-in ou um painel de controle, você poderá usar o método descrito nesta seção para habilitar um assembly para seu aplicativo. Para obter mais informações sobre como adicionar um assembly a aplicativos com extensões, consulte [habilitando um assembly em um aplicativo que hospeda uma dll, uma extensão ou um painel de controle](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**Para habilitar um assembly em um aplicativo sem componentes hospedados**

1.  Crie um manifesto que descreva a dependência do aplicativo ou da extensão no assembly.

    Por exemplo, o manifesto para "YourApplication" pode ser criado copiando o exemplo de manifesto a seguir e substituindo os valores corretos para **AssemblyIdentity**, **ProcessorArchitecture** e **Description**. Defina o valor de **ProcessorArchitecture** como x86 se estiver compilando em uma plataforma de 32 bits e para IA64 se estiver compilando em uma plataforma de 64 bits. O elemento **Description** contém uma descrição de opção do aplicativo. Para obter mais informações sobre o formato do manifesto, consulte [manifestos do aplicativo](application-manifests.md).

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Adicione o manifesto ao aplicativo como um recurso no arquivo de cabeçalho executável binário do aplicativo. Não é recomendável que você adicione o manifesto ao aplicativo como um arquivo de manifesto externo.

    Para adicionar o manifesto como um recurso, crie um recurso no aplicativo do tipo ID de \_ manifesto RT 1. Por exemplo, se o nome do aplicativo for YourApp, o arquivo de cabeçalho do aplicativo deverá conter o seguinte:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Se, em vez disso, você adicionar o manifesto como um arquivo de manifesto externo, certifique-se de que a instalação copie o arquivo de manifesto na pasta que contém o arquivo executável do aplicativo.

3.  Teste para garantir que os assemblies usados pelo aplicativo funcionem corretamente no aplicativo.

 

 



