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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Acessar variáveis de firmware UEFI de um aplicativo universal do Windows

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Como acessar variáveis de firmware Unified Extensible Firmware Interface (UEFI) de um aplicativo universal do Windows.

A partir do Windows 10, versão 1803, os aplicativos universais do Windows podem usar [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) e [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (e suas variantes ' ex ') para acessar variáveis de firmware UEFI fazendo o seguinte:

-   Declare a funcionalidade personalizada **Microsoft. firmwareRead \_ cw5n1h2txyewy** no manifesto para ler uma variável de firmware e/ou o recurso **Microsoft. firmwareWrite \_ cw5n1h2txyewy** para gravar uma variável de firmware.
-   Declare também o recurso restrito **protectedApp** no manifesto do aplicativo.
-   Por exemplo, as seguintes adições de manifesto de aplicativo permitem que o aplicativo universal do Windows Leia as variáveis de firmware:

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

-   Defina a opção de vinculador **/INTEGRITYCHECK** para todas as configurações de projeto, antes de enviar o aplicativo para a Microsoft Store. Isso garante que o aplicativo será iniciado como um aplicativo protegido. Consulte [/INTEGRITYCHECK (exigir verificação de assinatura)](/cpp/build/reference/integritycheck-require-signature-check) para obter detalhes.
-   Obtenha um arquivo SCCD ( [descritor de recurso personalizado assinado](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) ) da Microsoft. Consulte [criando um recurso personalizado para emparelhar um driver com um aplicativo de suporte de hardware (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) e [usando uma funcionalidade personalizada para emparelhar um aplicativo de suporte de hardware (HSA) com um driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) para obter informações sobre como obter o arquivo SCCD assinado da Microsoft, como empacotá-lo com seu aplicativo e como habilitar o modo de desenvolvedor. Aqui está um exemplo de arquivo SSCD do [exemplo CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):
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

    

-   Envie o aplicativo para o Microsoft Store para que ele seja assinado. Para fins de desenvolvimento, você pode ignorar a assinatura habilitando a assinatura de teste no banco de dados de configuração de inicialização (BCD). Consulte [a opção de configuração de inicialização testsigning](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) para obter detalhes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funcionalidades especiais e restritas](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**GetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**SetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Acessar informações de SMBIOS de um aplicativo universal do Windows](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
