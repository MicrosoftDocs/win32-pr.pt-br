---
description: O exemplo a seguir discute como gerar um assembly lado a lado assinado que consiste no manifesto do assembly, no catálogo de verificação e nos arquivos de assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Exemplo de assinatura de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105747244"
---
# <a name="assembly-signing-example"></a>Exemplo de assinatura de assembly

O exemplo a seguir discute como gerar um assembly lado a lado assinado que consiste no manifesto do assembly, no catálogo de verificação e nos arquivos de assembly. Assemblies compartilhados lado a lado devem ser assinados. O sistema operacional verifica a assinatura do assembly antes de instalar um assembly compartilhado no repositório global lado a lado (WinSxS). Isso dificulta a falsificação do editor do assembly lado a lado.

Observe que alterar os arquivos de assembly ou o conteúdo do manifesto depois de gerar o catálogo de assembly invalida o catálogo e o assembly. Se for necessário atualizar os arquivos de assembly ou o manifesto depois de criar e assinar o catálogo, você deverá assinar novamente o assembly e gerar um novo catálogo.

Comece com os arquivos de assembly, o manifesto do assembly e o arquivo de certificado que você usará para assinar o assembly. O arquivo de certificado deve ter 2048 bits ou mais. Não é necessário usar um certificado confiável. O certificado é usado somente para verificar se o assembly não foi danificado.

Execute o utilitário [Pktextract.exe](pktextract-exe.md) fornecido no SDK (Software Development Kit) do Microsoft Windows para extrair o token de chave pública do arquivo de certificado. Para que o Pktextract funcione corretamente, o arquivo de certificado deve estar presente no mesmo diretório que o utilitário. Use o valor do token de chave pública extraído para atualizar o atributo **PublicKeyToken** do elemento **AssemblyIdentity** no arquivo de manifesto.

Aqui está um exemplo de um arquivo de manifesto chamado MySampleAssembly. manifest. O assembly MySampleAssembly contém apenas um arquivo, MYFILE.DLL. Observe que o valor do atributo **PublicKeyToken** do elemento **AssemblyIdentity** foi atualizado com o valor do token de chave pública.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

Em seguida, execute o utilitário [Mt.exe](mt-exe.md) fornecido no SDK do Windows. Os arquivos de assembly devem estar localizados no mesmo diretório que o manifesto. Neste exemplo, esse é o diretório MySampleAssembly. Chame Mt.exe para o exemplo da seguinte maneira:

**c: \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**

Veja a seguir como o manifesto de exemplo é exibido após a execução de Mt.exe. Observe que a execução de Mt.exe com a opção hashupdate adiciona o hash SHA-1 do arquivo. Não altere esse valor.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

A execução de Mt.exe com a opção-makecdfs gera um arquivo chamado MySampleAssembly. manifest. CDF que descreve o conteúdo do catálogo de segurança que será usado para validar o manifesto.

A próxima etapa é executar Makecat.exe sobre este. CDF para criar o catálogo de segurança para o assembly. A chamada para Makecat.exe para este exemplo seria exibida da seguinte maneira:

**c: \\ MySampleAssembly>Makecat MySampleAssembly. manifest. CDF**

A etapa final é executar SignTool.exe para assinar o arquivo de catálogo com o certificado. Esse deve ser o mesmo certificado que foi usado no anterior para gerar o token de chave pública. Para obter mais informações sobre SignTool.exe consulte o tópico [**SignTool**](../seccrypto/signtool.md) . A chamada para **SignTool** para o exemplo seria exibida da seguinte maneira:

**c: \\ MySampleAssembly>Signtool sinal/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.Cat**

Se você tiver um certificado digital autenticado e sua autoridade de certificação usar o formato de arquivo PVK para armazenar a chave privada, você poderá usar o serviço de certificados de certificado digital do PVK (pvkimprt.exe) para importar a chave para o CSP (provedor de serviços de criptografia). Esse utilitário permite que você exporte para o formato padrão do setor PFX/P12. Para obter mais informações sobre o importador de arquivos de certificado digital PVK, consulte a seção recursos de implantação da biblioteca MSDN ou entre em contato com sua autoridade de certificação. Talvez você possa obter pvkimprt.exe do https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Consulte também [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).

 

 
