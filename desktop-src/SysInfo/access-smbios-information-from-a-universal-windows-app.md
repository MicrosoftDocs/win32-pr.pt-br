---
description: Como acessar informações do SMBIOS (BIOS de gerenciamento do sistema) de um aplicativo universal do Windows.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Acessar informações de SMBIOS de um aplicativo universal do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505949"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Acessar informações de SMBIOS de um aplicativo universal do Windows

> ANOTAÇÕES Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.

Como acessar informações do SMBIOS (BIOS de gerenciamento do sistema) de um aplicativo universal do Windows.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Acessar informações de SMBIOS de um aplicativo Plataforma Universal do Windows

A partir do Windows 10, versão 1803, os aplicativos universais do Windows podem usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) e [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acessar informações de SMBIOS declarando a capacidade restrita de **SMBIOS** no manifesto do aplicativo.

> [!IMPORTANT]
> Somente o acesso a tabelas de firmware RSMB (SMBIOS brutos) tem suporte de um aplicativo universal do Windows. **Acesso \_ ao NEGAdo** será retornado se você tentar acessar outros tipos de tabela de firmware de um aplicativo universal do Windows.

 

Para declarar o recurso de **SMBIOS** Restricted no manifesto do aplicativo, adicione o namespace **rescap** e o recurso **SMBIOS** da seguinte maneira:

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funcionalidades especiais e restritas](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[Acessar variáveis de firmware UEFI de um aplicativo universal do Windows](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
