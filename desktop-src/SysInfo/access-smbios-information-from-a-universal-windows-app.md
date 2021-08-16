---
description: como acessar informações do SMBIOS (BIOS de gerenciamento do sistema) de um aplicativo Universal Windows.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: acessar informações de SMBIOS de um aplicativo Universal Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764950"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>acessar informações de SMBIOS de um aplicativo Universal Windows

> ANOTAÇÕES Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.

como acessar informações do SMBIOS (BIOS de gerenciamento do sistema) de um aplicativo Universal Windows.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>acessar informações de SMBIOS de um aplicativo Plataforma Universal do Windows

a partir do Windows 10, a versão 1803, aplicativos de Windows Universal podem usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) e [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acessar informações de smbios declarando a capacidade restrita de **smbios** no manifesto do aplicativo.

> [!IMPORTANT]
> somente o acesso a tabelas de firmware RSMB (SMBIOS brutos) tem suporte de um aplicativo Universal Windows. **Acesso \_ ao negado** será retornado se você tentar acessar outros tipos de tabela de firmware de um aplicativo Universal Windows.

 

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

[acessar variáveis de firmware UEFI de um aplicativo Universal Windows](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
