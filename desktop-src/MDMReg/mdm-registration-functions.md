---
title: Funções de registro do MDM
description: As funções a seguir são declaradas em `mdmregistration.h` e são usadas pelo registro do MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: f9149c4bd2f9f931a506dc35d05b5e1c641dc87445fbf88fd73ff9ad20ac514b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040366"
---
# <a name="mdm-registration-functions"></a>Funções de registro do MDM

As funções a seguir são declaradas em `mdmregistration.h` e são usadas pelo registro do MDM.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Descobre o serviço MDM. |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Descobre o serviço MDM usando um servidor candidato. |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Obtém as informações de configuração associadas à ID do provedor. |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Recupera as informações de registro do dispositivo. |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Recupera o hiperlink do aplicativo de gerenciamento associado ao serviço MDM. |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Verifica se o dispositivo está registrado com um serviço MDM. |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Verifica se o registro de MDM é permitido pela política local. |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Registra um dispositivo com um serviço MDM, usando o [ \[ \] protocolo de registro de dispositivo móvel MS-MDE:](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267). |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | registra um dispositivo com um serviço MDM, usando as credenciais do Azure Active Directory (AAD). |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Define as informações de configuração associadas à ID do provedor. |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Indica ao agente MDM que o dispositivo é gerenciado externamente e não deve ser registrado com um serviço MDM. |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Cancela o registro de um dispositivo com o serviço MDM. |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de registro do MDM](./mdm-registration-reference.md)
