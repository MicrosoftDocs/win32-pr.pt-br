---
title: Interface IWMDRMDevice
description: Essa interface não se destina a ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa. A interface IWMDRMDevice permite que um provedor de conteúdo seguro se comunique com dispositivos que usam Windows DRM de Mídia 10 para Dispositivos Portáteis.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , descrito
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fee40eb6fdada2374b0f571a201ff53fb38f41de7f3cac5eeaa2159475bfdb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005116"
---
# <a name="iwmdrmdevice-interface"></a>Interface IWMDRMDevice

Essa interface não se destina a ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa.

A interface **IWMDRMDevice** permite que um provedor de conteúdo seguro se comunique com dispositivos que usam Windows DRM de Mídia 10 para Dispositivos Portáteis.

## <a name="members"></a>Membros

A interface **IWMDRMDevice** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDevice** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDevice** tem esses métodos.



| Método                                                                  | Descrição                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera o certificado do dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera o desafio de medição.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera o relógio seguro.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera o desafio de relógio seguro.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Recupera a lista de sincronização de licenças.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina se o dispositivo dá suporte Windows DRM de Mídia 10 para Dispositivos Portáteis.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Define a resposta da licença.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Define a resposta de medição.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Define a resposta do relógio seguro.<br/>                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para provedores de serviços**](interfaces-for-service-providers.md)
</dt> </dl>

 

