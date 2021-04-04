---
title: Como criar um certificado de assinatura de pacote de aplicativos
description: Saiba como usar MakeCert.exe e Pvk2Pfx.exe para criar um certificado de assinatura de código de teste, para que você possa assinar seus pacotes de aplicativos do Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007372"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="022e7-103">Como criar um certificado de assinatura de pacote de aplicativos</span><span class="sxs-lookup"><span data-stu-id="022e7-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="022e7-104">MakeCert.exe é preterida.</span><span class="sxs-lookup"><span data-stu-id="022e7-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="022e7-105">Para obter as diretrizes atuais sobre a criação de um certificado, consulte [criar um certificado para assinatura de pacote](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="022e7-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="022e7-106">Saiba como usar [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) para criar um certificado de assinatura de código de teste, para que você possa assinar seus pacotes de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="022e7-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="022e7-107">Você deve assinar digitalmente seus aplicativos do Windows empacotados antes de implantá-los.</span><span class="sxs-lookup"><span data-stu-id="022e7-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="022e7-108">Se você não usar Microsoft Visual Studio 2012 para criar e assinar seus pacotes de aplicativos, você precisará criar e gerenciar seus próprios certificados de assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="022e7-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="022e7-109">Você pode criar certificados usando [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) do Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="022e7-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="022e7-110">Em seguida, você pode usar os certificados para assinar os pacotes de aplicativos, para que eles possam ser implantados localmente para teste.</span><span class="sxs-lookup"><span data-stu-id="022e7-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="022e7-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="022e7-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="022e7-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="022e7-112">Technologies</span></span>

-   <span data-ttu-id="022e7-113">[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="022e7-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="022e7-114">[Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="022e7-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="022e7-115">Ferramentas para assinar drivers</span><span class="sxs-lookup"><span data-stu-id="022e7-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="022e7-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="022e7-116">Prerequisites</span></span>

-   <span data-ttu-id="022e7-117">Ferramentas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) do WDK</span><span class="sxs-lookup"><span data-stu-id="022e7-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="022e7-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="022e7-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="022e7-119">Etapa 1: determinar o nome do editor do pacote</span><span class="sxs-lookup"><span data-stu-id="022e7-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="022e7-120">Para tornar o certificado de autenticação que você cria utilizável com o pacote do aplicativo que você deseja assinar, o nome da entidade do certificado de autenticação deve corresponder ao atributo **Publisher** do elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml para esse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="022e7-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="022e7-121">Por exemplo, suponha que o AppxManifest.xml contenha:</span><span class="sxs-lookup"><span data-stu-id="022e7-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="022e7-122">Para o parâmetro *PublisherName* que você especificar com o utilitário [**MakeCert**](/windows-hardware/drivers/devtest/makecert) na próxima etapa, use "CN = Contoso software, O = Contoso Corporation, C = US".</span><span class="sxs-lookup"><span data-stu-id="022e7-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="022e7-123">Essa cadeia de caracteres de parâmetro é especificada entre aspas e diferencia maiúsculas de minúsculas e espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="022e7-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="022e7-124">A cadeia de caracteres de atributo do **Publicador** definida para o elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml deve ser idêntica à cadeia de caracteres que você especificar com o parâmetro [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n para o nome da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="022e7-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="022e7-125">Copie e cole a cadeia de caracteres sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="022e7-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="022e7-126">Etapa 2: criar uma chave privada usando MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="022e7-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="022e7-127">Use o utilitário [**MakeCert**](/windows-hardware/drivers/devtest/makecert) para criar um certificado de teste autoassinado e uma chave privada:</span><span class="sxs-lookup"><span data-stu-id="022e7-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="022e7-128">Esse comando solicita que você forneça uma senha para o arquivo. pvk.</span><span class="sxs-lookup"><span data-stu-id="022e7-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="022e7-129">Recomendamos que você escolha uma [senha forte](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) e mantenha sua chave privada em um local seguro.</span><span class="sxs-lookup"><span data-stu-id="022e7-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="022e7-130">É recomendável que você use os parâmetros sugeridos no exemplo anterior por estes motivos:</span><span class="sxs-lookup"><span data-stu-id="022e7-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="022e7-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="022e7-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="022e7-132">Cria um certificado raiz autoassinado.</span><span class="sxs-lookup"><span data-stu-id="022e7-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="022e7-133">Isso simplifica o gerenciamento do seu certificado de teste.</span><span class="sxs-lookup"><span data-stu-id="022e7-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="022e7-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="022e7-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="022e7-135">Marca a restrição básica para o certificado como uma entidade final.</span><span class="sxs-lookup"><span data-stu-id="022e7-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="022e7-136">Isso impede que o certificado seja usado como uma autoridade de certificação (CA) que pode emitir outros certificados.</span><span class="sxs-lookup"><span data-stu-id="022e7-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="022e7-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="022e7-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="022e7-138">Define os valores de EKU (uso avançado de chave) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="022e7-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="022e7-139">Não coloque um espaço entre os dois valores delimitados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="022e7-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="022e7-140">1.3.6.1.5.5.7.3.3 indica que o certificado é válido para assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="022e7-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="022e7-141">Sempre Especifique esse valor para limitar o uso pretendido para o certificado.</span><span class="sxs-lookup"><span data-stu-id="022e7-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="022e7-142">1.3.6.1.4.1.311.10.3.13 indica que o certificado respeita o tempo de vida da assinatura.</span><span class="sxs-lookup"><span data-stu-id="022e7-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="022e7-143">Normalmente, se uma assinatura tiver o carimbo de data/hora, desde que o certificado tenha sido válido no ponto em que estava carimbado, a assinatura permanecerá válida mesmo se o certificado expirar.</span><span class="sxs-lookup"><span data-stu-id="022e7-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="022e7-144">Esse EKU força a assinatura a expirar, independentemente de a assinatura ser carimbada pelo tempo.</span><span class="sxs-lookup"><span data-stu-id="022e7-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="022e7-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="022e7-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="022e7-146">Define a data de validade do certificado.</span><span class="sxs-lookup"><span data-stu-id="022e7-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="022e7-147">Forneça um valor para o parâmetro *expirationDate* no formato mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="022e7-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="022e7-148">Recomendamos que você escolha uma data de expiração somente se necessário para seus fins de teste, normalmente menos de um ano.</span><span class="sxs-lookup"><span data-stu-id="022e7-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="022e7-149">Essa data de expiração em conjunto com o EKU de assinatura de tempo de vida pode ajudar a limitar a janela em que o certificado pode ser comprometido e usado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="022e7-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="022e7-150">Para obter mais informações sobre outras opções, consulte [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="022e7-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="022e7-151">Etapa 3: criar um arquivo de troca de informações pessoais (. pfx) usando Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="022e7-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="022e7-152">Use o utilitário [**pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para converter os arquivos. pvk e. cer que o [**MakeCert**](/windows-hardware/drivers/devtest/makecert) criou em um arquivo. pfx que você pode usar com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="022e7-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="022e7-153">Os arquivos *myKey. pvk* e *myKey. cer* são os mesmos arquivos que [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) criados na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="022e7-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="022e7-154">Usando o parâmetro opcional/Po, você pode especificar uma senha diferente para o. pfx resultante; caso contrário, o. pfx terá a mesma senha que *myKey. pvk*.</span><span class="sxs-lookup"><span data-stu-id="022e7-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="022e7-155">Para obter mais informações sobre outras opções, consulte [**pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="022e7-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="022e7-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="022e7-156">Remarks</span></span>

<span data-ttu-id="022e7-157">Depois de criar o arquivo. pfx, você pode usar o arquivo com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="022e7-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="022e7-158">Para obter mais informações, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="022e7-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="022e7-159">Mas o certificado ainda não é confiável para o computador local para implantação de pacotes de aplicativos até que você o instale no repositório de certificados confiáveis do computador local.</span><span class="sxs-lookup"><span data-stu-id="022e7-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="022e7-160">Você pode usar [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), que vem com o Windows.</span><span class="sxs-lookup"><span data-stu-id="022e7-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="022e7-161">**Para instalar certificados com WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="022e7-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="022e7-162">Execute **Cmd.exe** como administrador.</span><span class="sxs-lookup"><span data-stu-id="022e7-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="022e7-163">Execute este comando:</span><span class="sxs-lookup"><span data-stu-id="022e7-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="022e7-164">Recomendamos que você remova os certificados se eles não estiverem mais em uso.</span><span class="sxs-lookup"><span data-stu-id="022e7-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="022e7-165">No mesmo prompt de comando do administrador, execute este comando:</span><span class="sxs-lookup"><span data-stu-id="022e7-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="022e7-166">**Certid** é o número de série do certificado.</span><span class="sxs-lookup"><span data-stu-id="022e7-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="022e7-167">Execute este comando para determinar o número de série do certificado:</span><span class="sxs-lookup"><span data-stu-id="022e7-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="022e7-168">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="022e7-168">Security Considerations</span></span>

<span data-ttu-id="022e7-169">Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="022e7-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="022e7-170">Recomendamos que você instale todos os certificados de assinatura de código desejados para testar pacotes de aplicativos no repositório de certificados de pessoas confiáveis.</span><span class="sxs-lookup"><span data-stu-id="022e7-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="022e7-171">Remova imediatamente esses certificados quando eles não forem mais necessários, para impedir que eles sejam usados para comprometer a confiança do sistema.</span><span class="sxs-lookup"><span data-stu-id="022e7-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="022e7-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="022e7-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="022e7-173">**Amostras**</span><span class="sxs-lookup"><span data-stu-id="022e7-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="022e7-174">Criar exemplo de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="022e7-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="022e7-175">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="022e7-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="022e7-176">[Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="022e7-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="022e7-177">Como assinar um pacote de aplicativos usando o SignTool</span><span class="sxs-lookup"><span data-stu-id="022e7-177">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

<span data-ttu-id="022e7-178">[Assinar um pacote do aplicativo](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="022e7-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 