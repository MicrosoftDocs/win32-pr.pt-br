---
title: Interface IWMDRMDeviceApp2
description: A interface IWMDRMDeviceApp2 estende o IWMDRMDeviceApp fornecendo uma nova versão do método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293391"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interface IWMDRMDeviceApp2

A interface **IWMDRMDeviceApp2** estende o [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornecendo uma nova versão do método [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) . O **QueryDeviceStatus2** permite que o chamador consulte um requisito de DRM específico.

Para obter essa interface, chame **CoCreateInstance** e transmita \_ WMDRMDeviceApp CLSID.

> [!Note]  
> Essa interface é definida no arquivo de cabeçalho criado a partir de WMDRMDeviceApp. idl. Esse cabeçalho **\# inclui** "WMDM. h". Talvez seja necessário alterar esse nome de arquivo para corresponder ao cabeçalho criado a partir de WMDM. idl.

 

## <a name="members"></a>Membros

A interface **IWMDRMDeviceApp2** herda de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMDeviceApp2** tem esses métodos.



| Método                                                            | Descrição                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Consulta um dispositivo em busca de um status ou recurso DRM específico.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Lidando com conteúdo protegido no aplicativo**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicativos**](interfaces-for-applications.md)
</dt> <dt>

[**Uso de conteúdo de medição**](metering-content-usage.md)
</dt> </dl>

 

 





