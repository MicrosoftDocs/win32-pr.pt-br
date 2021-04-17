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
# <a name="assembly-signing-example"></a><span data-ttu-id="cbb27-103">Exemplo de assinatura de assembly</span><span class="sxs-lookup"><span data-stu-id="cbb27-103">Assembly Signing Example</span></span>

<span data-ttu-id="cbb27-104">O exemplo a seguir discute como gerar um assembly lado a lado assinado que consiste no manifesto do assembly, no catálogo de verificação e nos arquivos de assembly.</span><span class="sxs-lookup"><span data-stu-id="cbb27-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="cbb27-105">Assemblies compartilhados lado a lado devem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="cbb27-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="cbb27-106">O sistema operacional verifica a assinatura do assembly antes de instalar um assembly compartilhado no repositório global lado a lado (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="cbb27-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="cbb27-107">Isso dificulta a falsificação do editor do assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="cbb27-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="cbb27-108">Observe que alterar os arquivos de assembly ou o conteúdo do manifesto depois de gerar o catálogo de assembly invalida o catálogo e o assembly.</span><span class="sxs-lookup"><span data-stu-id="cbb27-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="cbb27-109">Se for necessário atualizar os arquivos de assembly ou o manifesto depois de criar e assinar o catálogo, você deverá assinar novamente o assembly e gerar um novo catálogo.</span><span class="sxs-lookup"><span data-stu-id="cbb27-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="cbb27-110">Comece com os arquivos de assembly, o manifesto do assembly e o arquivo de certificado que você usará para assinar o assembly.</span><span class="sxs-lookup"><span data-stu-id="cbb27-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="cbb27-111">O arquivo de certificado deve ter 2048 bits ou mais.</span><span class="sxs-lookup"><span data-stu-id="cbb27-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="cbb27-112">Não é necessário usar um certificado confiável.</span><span class="sxs-lookup"><span data-stu-id="cbb27-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="cbb27-113">O certificado é usado somente para verificar se o assembly não foi danificado.</span><span class="sxs-lookup"><span data-stu-id="cbb27-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="cbb27-114">Execute o utilitário [Pktextract.exe](pktextract-exe.md) fornecido no SDK (Software Development Kit) do Microsoft Windows para extrair o token de chave pública do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="cbb27-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="cbb27-115">Para que o Pktextract funcione corretamente, o arquivo de certificado deve estar presente no mesmo diretório que o utilitário.</span><span class="sxs-lookup"><span data-stu-id="cbb27-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="cbb27-116">Use o valor do token de chave pública extraído para atualizar o atributo **PublicKeyToken** do elemento **AssemblyIdentity** no arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="cbb27-117">Aqui está um exemplo de um arquivo de manifesto chamado MySampleAssembly. manifest.</span><span class="sxs-lookup"><span data-stu-id="cbb27-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="cbb27-118">O assembly MySampleAssembly contém apenas um arquivo, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="cbb27-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="cbb27-119">Observe que o valor do atributo **PublicKeyToken** do elemento **AssemblyIdentity** foi atualizado com o valor do token de chave pública.</span><span class="sxs-lookup"><span data-stu-id="cbb27-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

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

<span data-ttu-id="cbb27-120">Em seguida, execute o utilitário [Mt.exe](mt-exe.md) fornecido no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="cbb27-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="cbb27-121">Os arquivos de assembly devem estar localizados no mesmo diretório que o manifesto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="cbb27-122">Neste exemplo, esse é o diretório MySampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="cbb27-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="cbb27-123">Chame Mt.exe para o exemplo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cbb27-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="cbb27-124">**c: \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="cbb27-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="cbb27-125">Veja a seguir como o manifesto de exemplo é exibido após a execução de Mt.exe.</span><span class="sxs-lookup"><span data-stu-id="cbb27-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="cbb27-126">Observe que a execução de Mt.exe com a opção hashupdate adiciona o hash SHA-1 do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cbb27-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="cbb27-127">Não altere esse valor.</span><span class="sxs-lookup"><span data-stu-id="cbb27-127">Do not change this value.</span></span>

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

<span data-ttu-id="cbb27-128">A execução de Mt.exe com a opção-makecdfs gera um arquivo chamado MySampleAssembly. manifest. CDF que descreve o conteúdo do catálogo de segurança que será usado para validar o manifesto.</span><span class="sxs-lookup"><span data-stu-id="cbb27-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="cbb27-129">A próxima etapa é executar Makecat.exe sobre este. CDF para criar o catálogo de segurança para o assembly.</span><span class="sxs-lookup"><span data-stu-id="cbb27-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="cbb27-130">A chamada para Makecat.exe para este exemplo seria exibida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cbb27-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="cbb27-131">**c: \\ MySampleAssembly>Makecat MySampleAssembly. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="cbb27-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="cbb27-132">A etapa final é executar SignTool.exe para assinar o arquivo de catálogo com o certificado.</span><span class="sxs-lookup"><span data-stu-id="cbb27-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="cbb27-133">Esse deve ser o mesmo certificado que foi usado no anterior para gerar o token de chave pública.</span><span class="sxs-lookup"><span data-stu-id="cbb27-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="cbb27-134">Para obter mais informações sobre SignTool.exe consulte o tópico [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb27-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="cbb27-135">A chamada para **SignTool** para o exemplo seria exibida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cbb27-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="cbb27-136">**c: \\ MySampleAssembly>Signtool sinal/f \<fullpath> MyCompany. pfx/du https: \/ /www.mycompany.com/MySampleAssembly/t https: \/ /timestamp.DigiCert.com MySampleAssembly.Cat**</span><span class="sxs-lookup"><span data-stu-id="cbb27-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="cbb27-137">Se você tiver um certificado digital autenticado e sua autoridade de certificação usar o formato de arquivo PVK para armazenar a chave privada, você poderá usar o serviço de certificados de certificado digital do PVK (pvkimprt.exe) para importar a chave para o CSP (provedor de serviços de criptografia).</span><span class="sxs-lookup"><span data-stu-id="cbb27-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="cbb27-138">Esse utilitário permite que você exporte para o formato padrão do setor PFX/P12.</span><span class="sxs-lookup"><span data-stu-id="cbb27-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="cbb27-139">Para obter mais informações sobre o importador de arquivos de certificado digital PVK, consulte a seção recursos de implantação da biblioteca MSDN ou entre em contato com sua autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="cbb27-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="cbb27-140">Talvez você possa obter pvkimprt.exe do https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="cbb27-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="cbb27-141">Consulte também [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="cbb27-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
