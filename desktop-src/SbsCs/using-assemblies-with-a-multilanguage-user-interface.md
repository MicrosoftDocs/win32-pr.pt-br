---
description: Se você quiser que os usuários do seu aplicativo, ou a DLL principal, sejam capazes de alterar o idioma da interface do usuário, considere colocar recursos de idioma em DLLs de recurso satélite separadas.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Usando assemblies com uma interface de usuário multilíngüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647011"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Usando assemblies com uma interface de usuário multilíngüe

Se você quiser que os usuários do seu aplicativo, ou a DLL principal, sejam capazes de alterar o idioma da interface do usuário, considere colocar recursos de idioma em DLLs de recurso satélite separadas. Para obter mais informações sobre como usar DLLs de recursos de satélite, consulte [Multilingual User interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).

Cada DLL satélite contém os recursos para um idioma diferente. A DLL principal pode ser fornecida como um assembly e cada uma das DLLs satélite pode ser fornecida como assemblies satélites separados. Nesse caso, cada assembly satélite deve ter seu próprio manifesto de assembly autodescritivo. O manifesto do assembly satélite não deve descrever nenhuma dependência em outros assemblies. Qualquer dependência de assemblies satélite em outros assemblies deve ser descrita no manifesto do assembly principal.

A versão [MUI (interface do usuário multilíngüe)](/windows/desktop/Intl/multilingual-user-interface) do Windows permite que os usuários especifiquem o idioma da interface do usuário de acordo com suas preferências, desde que o idioma necessário tenha sido adicionado ao sistema. Um assembly principal pode dar suporte a vários idiomas usando vários assemblies MUI. Nesse caso, cada assembly MUI deve ter seu próprio manifesto e qualquer dependência em relação a outros assemblies deve ser descrita apenas no manifesto do assembly principal.

Por exemplo, o proseware. Sample. pop pode ser um assembly lado a lado principal, que é dependente do assembly proseware. Research. SampleAssembly. Se o proseware. Sample. pop usar o MUI para dar suporte a vários idiomas, poderão ser fornecidos assemblies de MUI separados para cada idioma. Cada assembly do MUI deve ter seu próprio manifesto descrevendo essa DLL de recurso satélite específica. Os manifestos do assembly MUI não devem incluir nenhuma referência a dependências em outros assemblies. O manifesto que descreve o assembly principal, proseware. Sample. pop, deve descrever a dependência de Proseware. Sample. pop no assembly proseware. Research. SampleAssembly.

Os atributos do elemento **AssemblyIdentity** de um assembly satélite são semelhantes àqueles no manifesto do assembly de base. O atributo **Name** deve ser o mesmo que o assembly base com a adição de "Resources". Por exemplo, se o nome for "proseware. Tools. Verification. Runtime-Libraries" no assembly base, o nome no assembly de recursos seria "proseware. Tools. Verification. Runtime-Libraries. resources". O atributo **Language** deve identificar o idioma do assembly de recursos. O atributo de **arquivo** deve incluir a lista de arquivos que são DLLs de recurso.

Veja a seguir um exemplo do manifesto para o assembly de recursos do proseware. Tools. Verification. Runtime-Libraries.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

O assembly base descreve uma dependência opcional no assembly de recurso. Neste exemplo, se um usuário estiver executando o Windows com a localidade designada como alemão, um aplicativo que usa o assembly proseware. Tools. verificador ortográfico exibiria texto em alemão.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
