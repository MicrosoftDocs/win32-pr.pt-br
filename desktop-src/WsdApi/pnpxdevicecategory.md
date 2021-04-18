---
description: Especifica a categoria PnP-X à qual o dispositivo pertence. Mais de uma categoria pode ser especificada.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731dd78fbe366fc9c7923686d3d9ac90b772c23d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781577"
---
# <a name="pnpxdevicecategory-element"></a>Elemento PnPXDeviceCategory

Especifica a categoria PnP-X à qual o dispositivo pertence. Mais de uma categoria pode ser especificada.

## <a name="usage"></a>Uso

``` syntax
<PnPXDeviceCategory/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   | Descrição                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define os metadados de modelo e fabricante para o dispositivo a ser implementado.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os dispositivos também podem especificar uma subcategoria de dispositivo para uma categoria de dispositivo mais descritiva. Por exemplo, "phones. WindowsMobile cameras. DigitalStillCamera MediaDevices. MusicPlayer" identifica um dispositivo que é um dispositivo Microsoft Windows Mobile com uma câmera e um player de música. A categoria de dispositivo primário para este dispositivo seria "telefones".

Para especificar mais de uma categoria de dispositivo, separe as categorias com um espaço. Por exemplo, "armazenamento de impressoras" identifica um dispositivo com uma categoria primária de "impressoras" e uma categoria secundária de "armazenamento".

Se um elemento **PnPXDeviceCategory** estiver presente, pelo menos um elemento [**hospedado**](hosted.md) deverá conter ambos os elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId**](pnpxcompatibleid.md) . Da mesma forma, se os elementos **PnPXHardwareId** e **PnPXCompatibleId** estiverem presentes em um elemento **hospedado** , pelo menos um elemento **PnPXDeviceCategory** deverá estar presente dentro do elemento [**thisModelMetadata**](thismodelmetadata.md) .

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




