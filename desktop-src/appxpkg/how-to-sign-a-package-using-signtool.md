---
title: Como assinar um pacote do aplicativo usando a SignTool
description: Saiba como usar o SignTool para assinar seus pacotes de aplicativos do Windows para que eles possam ser implantados.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105764375"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="2bf55-103">Como assinar um pacote do aplicativo usando a SignTool</span><span class="sxs-lookup"><span data-stu-id="2bf55-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="2bf55-104">Para assinar um pacote de aplicativos do Windows, consulte [assinar um pacote de aplicativo usando Signtool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="2bf55-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="2bf55-105">Saiba como usar o [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativos do Windows para que eles possam ser implantados.</span><span class="sxs-lookup"><span data-stu-id="2bf55-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="2bf55-106">O [**SignTool**](/windows-hardware/drivers/devtest/signtool) faz parte do SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="2bf55-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="2bf55-107">Todos os pacotes de aplicativos do Windows devem ser assinados digitalmente antes que possam ser implantados.</span><span class="sxs-lookup"><span data-stu-id="2bf55-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="2bf55-108">Embora Microsoft Visual Studio 2012 e posterior possam assinar um pacote de aplicativo durante sua criação, os pacotes que você cria usando a ferramenta [MakeAppx.exe (App Packager)](make-appx-package--makeappx-exe-.md) do SDK do Windows não são assinados.</span><span class="sxs-lookup"><span data-stu-id="2bf55-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="2bf55-109">Você só pode usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativos do Windows no Windows 8 e posterior ou no windows Server 2012 e posterior.</span><span class="sxs-lookup"><span data-stu-id="2bf55-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="2bf55-110">Você não pode usar **SignTool** para assinar pacotes de aplicativos em sistemas operacionais de nível inferior, como o Windows 7 ou o windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="2bf55-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="2bf55-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="2bf55-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2bf55-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="2bf55-112">Technologies</span></span>

-   <span data-ttu-id="2bf55-113">[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bf55-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="2bf55-114">[Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="2bf55-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="2bf55-115">Ferramentas para assinar arquivos e verificar assinaturas</span><span class="sxs-lookup"><span data-stu-id="2bf55-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="2bf55-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf55-116">Prerequisites</span></span>

-   <span data-ttu-id="2bf55-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), que faz parte do SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="2bf55-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="2bf55-118">Um certificado de assinatura de código válido, por exemplo, um arquivo de troca de informações pessoais (. pfx) criado com as ferramentas [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)</span><span class="sxs-lookup"><span data-stu-id="2bf55-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="2bf55-119">Para obter informações sobre como criar um certificado de assinatura de código válido, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="2bf55-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="2bf55-120">Um aplicativo do Windows empacotado, por exemplo, um arquivo. Appx criado usando a ferramenta [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)</span><span class="sxs-lookup"><span data-stu-id="2bf55-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="2bf55-121">**Considerações adicionais**</span><span class="sxs-lookup"><span data-stu-id="2bf55-121">**Additional considerations**</span></span>

<span data-ttu-id="2bf55-122">O certificado que você usa para assinar o pacote de aplicativo deve atender a estes critérios:</span><span class="sxs-lookup"><span data-stu-id="2bf55-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="2bf55-123">O nome da entidade do certificado deve corresponder ao atributo de **Editor** contido no elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) do arquivo de AppxManifest.xml armazenado no pacote.</span><span class="sxs-lookup"><span data-stu-id="2bf55-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="2bf55-124">O nome do editor faz parte da identidade de um aplicativo do Windows empacotado, portanto, você precisa fazer com que o nome da entidade do certificado corresponda ao nome do editor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="2bf55-125">Isso permite que a identidade de pacotes assinados seja verificada em relação à assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="2bf55-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="2bf55-126">Para obter informações sobre erros de assinatura que podem surgir na assinatura de um pacote de aplicativo usando [**SignTool**](/windows-hardware/drivers/devtest/signtool), consulte a seção comentários de [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="2bf55-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="2bf55-127">O certificado deve ser válido para assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="2bf55-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="2bf55-128">Isso significa que ambos os itens devem ser verdadeiros:</span><span class="sxs-lookup"><span data-stu-id="2bf55-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="2bf55-129">O campo EKU (uso estendido de chave) do certificado deve ser desdefinido ou conter o valor de EKU para assinatura de código (1.3.6.1.5.5.7.3.3).</span><span class="sxs-lookup"><span data-stu-id="2bf55-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="2bf55-130">O campo uso de chave (KU) do certificado deve ser desdefinido ou conter o bit de uso para a assinatura digital (0x80).</span><span class="sxs-lookup"><span data-stu-id="2bf55-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="2bf55-131">O certificado contém uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="2bf55-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="2bf55-132">O certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="2bf55-132">The certificate is valid.</span></span> <span data-ttu-id="2bf55-133">Ele está ativo, não expirou e não foi revogado.</span><span class="sxs-lookup"><span data-stu-id="2bf55-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="2bf55-134">Instruções</span><span class="sxs-lookup"><span data-stu-id="2bf55-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="2bf55-135">Etapa 1: determinar o algoritmo de hash a ser usado</span><span class="sxs-lookup"><span data-stu-id="2bf55-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="2bf55-136">Ao assinar o pacote do aplicativo, você deve usar o mesmo algoritmo de hash que usou quando criou o pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="2bf55-137">Se você usou as configurações padrão para criar o pacote do aplicativo, o algoritmo de hash usado é SHA256.</span><span class="sxs-lookup"><span data-stu-id="2bf55-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="2bf55-138">Se você usou o app Packager com um algoritmo de hash específico para criar o pacote do aplicativo, use o mesmo algoritmo para assinar o pacote.</span><span class="sxs-lookup"><span data-stu-id="2bf55-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="2bf55-139">Para determinar o algoritmo de hash a ser usado para assinar um pacote, você pode extrair o conteúdo do pacote e inspecionar o arquivo de AppxBlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="2bf55-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="2bf55-140">O atributo **HashMethod** do elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica o algoritmo de hash que foi usado ao criar o pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="2bf55-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2bf55-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="2bf55-142">O elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) anterior indica que o algoritmo SHA256 foi usado.</span><span class="sxs-lookup"><span data-stu-id="2bf55-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="2bf55-143">Esta tabela lista o mapeamento dos algoritmos disponíveis no momento:</span><span class="sxs-lookup"><span data-stu-id="2bf55-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="2bf55-144">Valor de **HashMethod**</span><span class="sxs-lookup"><span data-stu-id="2bf55-144">**HashMethod** value</span></span>                            | <span data-ttu-id="2bf55-145">*hashAlgorithm* para usar</span><span class="sxs-lookup"><span data-stu-id="2bf55-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="2bf55-146">SHA256 (padrão. AppX)</span><span class="sxs-lookup"><span data-stu-id="2bf55-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="2bf55-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="2bf55-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="2bf55-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="2bf55-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="2bf55-149">Etapa 2: executar SignTool.exe para assinar o pacote</span><span class="sxs-lookup"><span data-stu-id="2bf55-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="2bf55-150">**Para assinar o pacote com um certificado de autenticação de um arquivo. pfx**</span><span class="sxs-lookup"><span data-stu-id="2bf55-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="2bf55-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) padroniza o parâmetro/FD *hashAlgorithm* para SHA1 se não for especificado, e SHA1 não é válido para assinar pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="2bf55-152">Portanto, você deve especificar esse parâmetro ao assinar um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="2bf55-153">Para assinar um pacote de aplicativo que foi criado com o hash SHA256 padrão, você especifica o parâmetro/FD *hashAlgorithm* como SHA256:</span><span class="sxs-lookup"><span data-stu-id="2bf55-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="2bf55-154">Você pode omitir o parâmetro/p *password* se usar um arquivo. pfx que não seja protegido por senha.</span><span class="sxs-lookup"><span data-stu-id="2bf55-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="2bf55-155">Você também pode usar outras opções de seleção de certificado com suporte de [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="2bf55-156">Para obter mais informações sobre essas opções, consulte [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="2bf55-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="2bf55-157">Não é possível usar a operação de carimbo de data/hora de [**SignTool**](/windows-hardware/drivers/devtest/signtool) em um pacote de aplicativo assinado; Não há suporte para a operação.</span><span class="sxs-lookup"><span data-stu-id="2bf55-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="2bf55-158">Se desejar marcar o data/hora do pacote do aplicativo, você deverá fazê-lo durante a operação de entrada.</span><span class="sxs-lookup"><span data-stu-id="2bf55-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="2bf55-159">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2bf55-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="2bf55-160">Torne o parâmetro/TR *timestampServerUrl* igual à URL de um servidor de carimbo de data/hora RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="2bf55-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf55-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bf55-161">Remarks</span></span>

<span data-ttu-id="2bf55-162">Esta seção aborda a solução de problemas de erros de assinatura para pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="2bf55-163">Solucionando problemas de erros de assinatura de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2bf55-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="2bf55-164">Além dos erros de assinatura que o [**SignTool**](/windows-hardware/drivers/devtest/signtool) pode retornar, o **SignTool** também pode retornar erros que são específicos para a assinatura de pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="2bf55-165">Esses erros geralmente aparecem como erros internos:</span><span class="sxs-lookup"><span data-stu-id="2bf55-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="2bf55-166">Se o código de erro começar com 0x8008, como o 0x80080206 APPX \_ E o \_ conteúdo corrompido \_ ), isso indicará que o pacote que está sendo assinado é inválido.</span><span class="sxs-lookup"><span data-stu-id="2bf55-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="2bf55-167">Nesse caso, antes de poder assinar o pacote, você deve recompilar o pacote.</span><span class="sxs-lookup"><span data-stu-id="2bf55-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="2bf55-168">Para obter a lista completa de \* erros de 0x8008, consulte [**códigos de erro com (segurança e configuração)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="2bf55-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="2bf55-169">Mais comumente, o erro é 0x8007000B ( \_ formato inadequado do erro \_ ).</span><span class="sxs-lookup"><span data-stu-id="2bf55-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="2bf55-170">Nesse caso, você pode encontrar informações de erro mais específicas no log de eventos:</span><span class="sxs-lookup"><span data-stu-id="2bf55-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="2bf55-171">**Para pesquisar o log de eventos**</span><span class="sxs-lookup"><span data-stu-id="2bf55-171">**To search the event log**</span></span>

1.  <span data-ttu-id="2bf55-172">Execute eventvwr. msc.</span><span class="sxs-lookup"><span data-stu-id="2bf55-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="2bf55-173">Abra o log de eventos: Visualizador de Eventos (local) > logs de aplicativos e serviços > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="2bf55-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="2bf55-174">Procure o evento de erro mais recente.</span><span class="sxs-lookup"><span data-stu-id="2bf55-174">Look for the most recent error event.</span></span>

<span data-ttu-id="2bf55-175">O erro interno geralmente corresponde a um destes:</span><span class="sxs-lookup"><span data-stu-id="2bf55-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bf55-176">ID do evento</span><span class="sxs-lookup"><span data-stu-id="2bf55-176">Event ID</span></span></th>
<th><span data-ttu-id="2bf55-177">Cadeia de caracteres de evento de exemplo</span><span class="sxs-lookup"><span data-stu-id="2bf55-177">Example event string</span></span></th>
<th><span data-ttu-id="2bf55-178">Sugestão</span><span class="sxs-lookup"><span data-stu-id="2bf55-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bf55-179">150</span><span class="sxs-lookup"><span data-stu-id="2bf55-179">150</span></span></td>
<td><span data-ttu-id="2bf55-180">Erro 0x8007000B: O nome do editor de manifesto de aplicativo (CN = Contoso) deve coincidir com o nome do requerente do certificado de autenticação (CN = Contoso, C = US).</span><span class="sxs-lookup"><span data-stu-id="2bf55-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="2bf55-181">O nome do editor de manifesto de aplicativo deve corresponder exatamente ao nome do assunto após a assinatura.</span><span class="sxs-lookup"><span data-stu-id="2bf55-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bf55-182">Esses nomes são especificados entre aspas e são diferenciais de maiúsculas e minúsculas e de espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="2bf55-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="2bf55-183">Você pode atualizar a cadeia de caracteres de atributo do <strong>Publicador</strong> que é definida para o elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> no arquivo AppxManifest.xml para corresponder ao nome da entidade do certificado de autenticação pretendido.</span><span class="sxs-lookup"><span data-stu-id="2bf55-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="2bf55-184">Ou então, selecione um certificado de autenticação diferente com um nome de entidade que corresponda ao nome do editor do manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="2bf55-185">O nome do editor do manifesto e o nome da entidade do certificado estão listados na mensagem do evento.</span><span class="sxs-lookup"><span data-stu-id="2bf55-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bf55-186">151</span><span class="sxs-lookup"><span data-stu-id="2bf55-186">151</span></span></td>
<td><span data-ttu-id="2bf55-187">Erro 0x8007000B: O método de hash de assinatura especificado (SHA512) deve coincidir com o método de hash usado no mapa de blocos do pacote de aplicativos (SHA256).</span><span class="sxs-lookup"><span data-stu-id="2bf55-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="2bf55-188">O hashAlgorithm especificado no parâmetro/FD está incorreto (consulte a etapa 1: determinar o algoritmo de hash a ser usado).</span><span class="sxs-lookup"><span data-stu-id="2bf55-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="2bf55-189">Execute o <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> novamente com o hashAlgorithm que corresponde ao mapa do bloco do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bf55-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bf55-190">152</span><span class="sxs-lookup"><span data-stu-id="2bf55-190">152</span></span></td>
<td><span data-ttu-id="2bf55-191">Erro 0x8007000B: O conteúdo do pacote de aplicativos deve ser validado em relação ao mapa de blocos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="2bf55-192">O pacote de aplicativos está corrompido e precisa ser recompilado para gerar um novo mapa de blocos.</span><span class="sxs-lookup"><span data-stu-id="2bf55-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="2bf55-193">Para obter mais informações sobre como criar um pacote de aplicativo, consulte Criando um pacote de aplicativo com o <a href="make-appx-package--makeappx-exe-.md">app Packager</a> ou <a href="/previous-versions/hh975357(v=vs.110)">criando um pacote de aplicativo com o Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="2bf55-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="2bf55-194">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="2bf55-194">Security Considerations</span></span>

<span data-ttu-id="2bf55-195">Depois que o pacote é assinado, o certificado que você usou para assinar o pacote ainda deve ser confiável pelo computador no qual o pacote será implantado.</span><span class="sxs-lookup"><span data-stu-id="2bf55-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="2bf55-196">Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="2bf55-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="2bf55-197">Recomendamos que você instale os certificados de assinatura de código que deseja para testar pacotes de aplicativos no repositório de certificados de pessoas confiáveis e remova esses certificados imediatamente quando não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="2bf55-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="2bf55-198">Se você criar seus próprios certificados de teste para assinar pacotes de aplicativos, também recomendamos que você restrinja os privilégios associados ao certificado de teste.</span><span class="sxs-lookup"><span data-stu-id="2bf55-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="2bf55-199">Para obter mais informações sobre como criar certificados de teste para assinar pacotes de aplicativos, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="2bf55-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bf55-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bf55-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2bf55-201">**Amostras**</span><span class="sxs-lookup"><span data-stu-id="2bf55-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="2bf55-202">Criar exemplo de pacote de aplicativo</span><span class="sxs-lookup"><span data-stu-id="2bf55-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="2bf55-203">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="2bf55-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="2bf55-204">[Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bf55-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2bf55-205">[Assinando um pacote no Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="2bf55-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="2bf55-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="2bf55-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="2bf55-207">App Packager (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="2bf55-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="2bf55-208">Como criar um certificado de assinatura de pacote de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2bf55-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

