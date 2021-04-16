---
description: Como acessar variáveis de firmware Unified Extensible Firmware Interface (UEFI) de um aplicativo universal do Windows.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Acessar variáveis de firmware UEFI de um aplicativo universal do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751058"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="6082a-103">Acessar variáveis de firmware UEFI de um aplicativo universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6082a-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="6082a-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="6082a-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6082a-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="6082a-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6082a-106">Como acessar variáveis de firmware Unified Extensible Firmware Interface (UEFI) de um aplicativo universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="6082a-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="6082a-107">A partir do Windows 10, versão 1803, os aplicativos universais do Windows podem usar [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) e [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (e suas variantes ' ex ') para acessar variáveis de firmware UEFI fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6082a-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="6082a-108">Declare a funcionalidade personalizada **Microsoft. firmwareRead \_ cw5n1h2txyewy** no manifesto para ler uma variável de firmware e/ou o recurso **Microsoft. firmwareWrite \_ cw5n1h2txyewy** para gravar uma variável de firmware.</span><span class="sxs-lookup"><span data-stu-id="6082a-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="6082a-109">Declare também o recurso restrito **protectedApp** no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6082a-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="6082a-110">Por exemplo, as seguintes adições de manifesto de aplicativo permitem que o aplicativo universal do Windows Leia as variáveis de firmware:</span><span class="sxs-lookup"><span data-stu-id="6082a-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="6082a-111">Defina a opção de vinculador **/INTEGRITYCHECK** para todas as configurações de projeto, antes de enviar o aplicativo para a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6082a-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="6082a-112">Isso garante que o aplicativo será iniciado como um aplicativo protegido.</span><span class="sxs-lookup"><span data-stu-id="6082a-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="6082a-113">Consulte [/INTEGRITYCHECK (exigir verificação de assinatura)](/cpp/build/reference/integritycheck-require-signature-check) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6082a-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="6082a-114">Obtenha um arquivo SCCD ( [descritor de recurso personalizado assinado](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) ) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6082a-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="6082a-115">Consulte [criando um recurso personalizado para emparelhar um driver com um aplicativo de suporte de hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) e [usando uma funcionalidade personalizada para emparelhar um aplicativo de suporte de hardware (HSA) com um driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) para obter informações sobre como obter o arquivo SCCD assinado da Microsoft, como empacotá-lo com seu aplicativo e como habilitar o modo de desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="6082a-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="6082a-116">Aqui está um exemplo de arquivo SSCD do [exemplo CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span><span class="sxs-lookup"><span data-stu-id="6082a-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="6082a-117">Envie o aplicativo para o Microsoft Store para que ele seja assinado.</span><span class="sxs-lookup"><span data-stu-id="6082a-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="6082a-118">Para fins de desenvolvimento, você pode ignorar a assinatura habilitando a assinatura de teste no banco de dados de configuração de inicialização (BCD).</span><span class="sxs-lookup"><span data-stu-id="6082a-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="6082a-119">Consulte [a opção de configuração de inicialização testsigning](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6082a-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6082a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6082a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6082a-121">Funcionalidades especiais e restritas</span><span class="sxs-lookup"><span data-stu-id="6082a-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="6082a-122">**GetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="6082a-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="6082a-123">**GetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="6082a-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="6082a-124">**SetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="6082a-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="6082a-125">**SetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="6082a-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="6082a-126">Acessar informações de SMBIOS de um aplicativo universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6082a-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
