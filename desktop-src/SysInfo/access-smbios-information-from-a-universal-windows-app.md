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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="6a6a2-103">Acessar informações de SMBIOS de um aplicativo universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6a6a2-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="6a6a2-104">ANOTAÇÕES Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6a6a2-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="6a6a2-106">Como acessar informações do SMBIOS (BIOS de gerenciamento do sistema) de um aplicativo universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="6a6a2-107">Acessar informações de SMBIOS de um aplicativo Plataforma Universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6a6a2-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="6a6a2-108">A partir do Windows 10, versão 1803, os aplicativos universais do Windows podem usar [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) e [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) para acessar informações de SMBIOS declarando a capacidade restrita de **SMBIOS** no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a6a2-109">Somente o acesso a tabelas de firmware RSMB (SMBIOS brutos) tem suporte de um aplicativo universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="6a6a2-110">**Acesso \_ ao NEGAdo** será retornado se você tentar acessar outros tipos de tabela de firmware de um aplicativo universal do Windows.</span><span class="sxs-lookup"><span data-stu-id="6a6a2-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="6a6a2-111">Para declarar o recurso de **SMBIOS** Restricted no manifesto do aplicativo, adicione o namespace **rescap** e o recurso **SMBIOS** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a6a2-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6a6a2-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a6a2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a6a2-113">Funcionalidades especiais e restritas</span><span class="sxs-lookup"><span data-stu-id="6a6a2-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="6a6a2-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="6a6a2-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="6a6a2-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="6a6a2-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="6a6a2-116">Acessar variáveis de firmware UEFI de um aplicativo universal do Windows</span><span class="sxs-lookup"><span data-stu-id="6a6a2-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
