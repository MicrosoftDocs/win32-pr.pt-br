---
description: Dá suporte à enumeração de interfaces IPortableDeviceConnector, representando dispositivos MTP/Bluetooth que foram emparelhados com o PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interface IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169559"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interface IEnumPortableDeviceConnectors

A interface **IEnumPortableDeviceConnectors** dá suporte à enumeração de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , representando dispositivos MTP/Bluetooth que foram emparelhados com o PC. Observe que isso recuperará todos os dispositivos emparelhados anteriormente, incluindo os dispositivos emparelhados, mas desconectados. Para determinar se um dispositivo ainda está conectado, consulte a propriedade **DEVPKEY \_ MTPBTH \_ IsConnected** para esse dispositivo.

## <a name="members"></a>Membros

A interface **IEnumPortableDeviceConnectors** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumPortableDeviceConnectors** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumPortableDeviceConnectors** tem esses métodos.



| Método                                               | Descrição                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**8i**](ienumportabledeviceconnectors-clone.md) | Cria uma cópia da interface **IEnumPortableDeviceConnectors** atual.<br/>                                                       |
| [**Avançar**](ienumportabledeviceconnectors-next.md)   | Recupera o próximo um ou mais objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) na sequência de enumeração.<br/> |
| [**Redefinir**](ienumportabledeviceconnectors-reset.md) | Redefine a sequência de enumeração para o início.<br/>                                                                                |
| [**Ignorar**](ienumportabledeviceconnectors-skip.md)   | Ignora o número especificado de dispositivos na sequência de enumeração.<br/>                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| parâmetro<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

