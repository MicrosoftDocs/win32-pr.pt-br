---
title: Interface IWMDRMDevice
description: Essa interface não deve ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa. A interface IWMDRMDevice permite que um provedor de conteúdo seguro se comunique com dispositivos que usam o Windows Media DRM 10 para dispositivos portáteis.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294173"
---
# <a name="iwmdrmdevice-interface"></a>Interface IWMDRMDevice

Essa interface não deve ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa.

A interface **IWMDRMDevice** permite que um provedor de conteúdo seguro se comunique com dispositivos que usam o Windows Media DRM 10 para dispositivos portáteis.

## <a name="members"></a>Membros

A interface **IWMDRMDevice** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDevice** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDevice** tem esses métodos.



| Método                                                                  | Descrição                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera o certificado do dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera o desafio de medição.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera o relógio seguro.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera o desafio do clock seguro.<br/>                                             |
| [**Getsincronizarlist**](iwmdrmdevice-getsynclist.md)                         | Recupera a lista de sincronização de licenças.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina se o dispositivo dá suporte a Windows Media DRM 10 para dispositivos portáteis.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Define a resposta da licença.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Define a resposta de medição.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Define a resposta de clock seguro.<br/>                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para provedores de serviços**](interfaces-for-service-providers.md)
</dt> </dl>

 

