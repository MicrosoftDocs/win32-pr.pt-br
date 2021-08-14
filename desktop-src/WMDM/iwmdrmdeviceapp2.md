---
title: Interface IWMDRMDeviceApp2
description: A interface IWMDRMDeviceApp2 estende IWMDRMDeviceApp fornecendo uma nova versão do método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interface IWMDRMDeviceApp2 windows Media Gerenciador de Dispositivos
- IWMDRMDeviceApp2 interface windows Media Gerenciador de Dispositivos , descrito
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584490"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interface IWMDRMDeviceApp2

A interface **IWMDRMDeviceApp2** estende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornecendo uma nova versão do [**método QueryDeviceStatus.**](iwmdrmdeviceapp-querydevicestatus.md) **QueryDeviceStatus2** permite que o chamador consulte um requisito de DRM específico.

Para obter essa interface, chame **CoCreateInstance** e passe CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Essa interface é definida no arquivo de header criado com base em WMDRMDeviceApp.idl. Esse header **\# inclui** "wmdm.h". Talvez seja necessário alterar esse nome de arquivo para corresponder ao header criado do WMDM.idl.

 

## <a name="members"></a>Membros

A interface **IWMDRMDeviceApp2** herda [**de IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDeviceApp2** tem esses métodos.



| Método                                                            | Descrição                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Consulta um dispositivo para um status ou funcionalidade de DRM específico.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Manipulando conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicativos**](interfaces-for-applications.md)
</dt> <dt>

[**Medição do uso de conteúdo**](metering-content-usage.md)
</dt> </dl>

 

 





