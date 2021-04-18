---
description: Se o seu aplicativo hospedar uma DLL, extensão, plug-in ou painel de controle de terceiros, convém habilitar um assembly em seu aplicativo&\# 8212; sem habilitar também esse assembly para os componentes hospedados.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Habilitando um assembly em um aplicativo que hospeda uma DLL, extensão ou painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748875"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Habilitando um assembly em um aplicativo que hospeda uma DLL, extensão ou painel de controle

Se o seu aplicativo hospedar uma DLL, extensão, plug-in ou painel de controle de terceiros, convém habilitar um assembly em seu aplicativo — sem habilitar também esse assembly para os componentes hospedados. Esse pode ser o caso quando um componente hospedado requer alterações de código para usar o assembly. Como desenvolvedor do aplicativo, talvez você não consiga fazer alterações nesses componentes de terceiros. Nesse caso, você deve seguir o procedimento descrito nesta seção para que seu aplicativo possa usar o assembly sem afetar os componentes hospedados.

-   Para habilitar um assembly em um aplicativo sem afetar DLLs hospedadas, extensões, plug-ins ou painéis de controle, um manifesto que descreve a dependência do aplicativo no assembly deve ser incluído no aplicativo como um recurso. Os componentes hospedados que não estão sendo habilitados com o assembly não devem incluir manifestos que descrevam essa dependência.
-   Para habilitar um assembly em um aplicativo e suas DLLs hospedadas, extensões, plug-ins ou painéis de controle, inclua manifestos como recursos no aplicativo e em seus componentes hospedados. Os manifestos incluídos no aplicativo e nos componentes hospedados devem descrever uma dependência no assembly. Normalmente, o desenvolvedor do aplicativo adiciona um manifesto ao aplicativo e o desenvolvedor do componente hospedado adiciona um manifesto à DLL, à extensão, ao plug-in ou ao painel de controle.

O método a seguir pode ser usado para adicionar um manifesto a um aplicativo ou a um componente hospedado que seja uma DLL, extensão, plug-in ou painel de controle.

**Para habilitar um assembly em um aplicativo ou componente hospedado.**

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

2.  Crie um recurso no aplicativo ou extensão do tipo ID de \_ manifesto RT 2.

    Por exemplo, se o nome do aplicativo for YourApp, o aplicativo deverá conter o seguinte:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  Compile o aplicativo com o sinalizador habilitado para reconhecimento de-DISOLATION \_ \_ ou insira essa instrução antes de \# incluir a instrução "Windows. h". No caso de um aplicativo com vários módulos, o \_ sinalizador habilitado para reconhecimento de DISOLATION \_ é necessário em todos os módulos.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Teste para garantir que os assemblies usados pelo aplicativo funcionem corretamente no aplicativo e no componente hospedado.

Para obter mais informações sobre como adicionar um assembly a aplicativos sem extensões, consulte [habilitando um assembly em um aplicativo sem extensões](enabling-an-assembly-in-an-application-without-extensions.md).

 

 



