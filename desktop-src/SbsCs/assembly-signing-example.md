---
description: O exemplo a seguir discute como gerar um assembly lado a lado assinado que consiste no manifesto do assembly, no catálogo de verificação e nos arquivos de assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Exemplo de assinatura de assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896da43b846edfd09348c6515fbf5e44fdd45dd2911b9fcdcf25e99f63fb6ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142459"
---
# <a name="assembly-signing-example"></a>Exemplo de assinatura de assembly

O exemplo a seguir discute como gerar um assembly lado a lado assinado que consiste no manifesto do assembly, no catálogo de verificação e nos arquivos de assembly. Assemblies compartilhados lado a lado devem ser assinados. O sistema operacional verifica a assinatura do assembly antes de instalar um assembly compartilhado no winSxS (armazenamento lado a lado global). Isso dificulta a spoof do editor do assembly lado a lado.

Observe que alterar os arquivos de assembly ou o conteúdo do manifesto depois de gerar o catálogo de assembly invalida o catálogo e o assembly. Se você precisa atualizar os arquivos de assembly ou manifesto depois de criar e assinar o catálogo, deverá assinar novamente o assembly e gerar um novo catálogo.

Comece com os arquivos de assembly, o manifesto do assembly e o arquivo de certificado que você usará para assinar o assembly. O arquivo de certificado deve ter 2.048 bits ou mais. Você não precisa usar um certificado confiável. O certificado é usado apenas para verificar se o assembly não foi danificado.

Execute o [Pktextract.exe](pktextract-exe.md) utilitário fornecido no SDK (Software Development Kit) do Microsoft Windows para extrair o token de chave pública do arquivo de certificado. Para que pktextract funcione corretamente, o arquivo de certificado deve estar presente no mesmo diretório que o utilitário . Use o valor do token de chave pública extraído para atualizar o **atributo publicKeyToken** do **elemento assemblyIdentity** no arquivo de manifesto.

Aqui está um exemplo de um arquivo de manifesto chamado MySampleAssembly.manifest. O assembly MySampleAssembly contém apenas um arquivo, MYFILE.DLL. Observe que o valor do **atributo publicKeyToken** do **elemento assemblyIdentity** foi atualizado com o valor do token de chave pública.

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

Em seguida, [executeMt.exe](mt-exe.md) utilitário fornecido no SDK do Windows. Os arquivos de assembly devem estar localizados no mesmo diretório que o manifesto. Neste exemplo, este é o diretório MySampleAssembly. Chame Mt.exe para o exemplo da seguinte forma:

**c: \\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**

Veja a aparência do manifesto de exemplo após a execução Mt.exe. Observe que executar Mt.exe com a opção hashupdate adiciona o hash SHA-1 do arquivo. Não altere esse valor.

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

Executar Mt.exe com a opção -makecdfs gera um arquivo chamado MySampleAssembly.manifest.cdf que descreve o conteúdo do catálogo de segurança que será usado para validar o manifesto.

A próxima etapa é executar Makecat.exe sobre esse .cdf para criar o catálogo de segurança para o assembly. A chamada para Makecat.exe para este exemplo seria exibida da seguinte forma:

**c: \\ MySampleAssembly>makecat MySampleAssembly.manifest.cdf**

A etapa final é executar SignTool.exe para assinar o arquivo de catálogo com o certificado. Esse deve ser o mesmo certificado que foi usado no anterior para gerar o token de chave pública. Para obter mais informações sobre SignTool.exe consulte o [**tópico SignTool.**](../seccrypto/signtool.md) A chamada para **SignTool** para o exemplo seria exibida da seguinte forma:

**c: \\ MySampleAssembly>signtool sign /f \<fullpath> mycompany.pfx /du https: \/ /www.mycompany.com/MySampleAssembly /t https: \/ /timestamp.digicert.com MySampleAssembly.cat**

Se você tiver um certificado digital autenticado e sua autoridade de certificação usar o formato de arquivo PVK para armazenar a chave privada, poderá usar o Importador de Arquivos de Certificado Digital (pvkimprt.exe) PVK para importar a chave para seu CSP (provedor de serviços criptográficos). Esse utilitário permite exportar para o formato padrão do setor PFX/P12. Para obter mais informações sobre o Importador de Arquivos de Certificado Digital PVK, consulte a seção Recursos de implantação da biblioteca MSDN ou entre em contato com sua autoridade de certificação. Você pode obter informações pvkimprt.exe de https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Consulte também Criando [arquivos assinados e catálogos](creating-signed-files-and-catalogs.md).

 

 
