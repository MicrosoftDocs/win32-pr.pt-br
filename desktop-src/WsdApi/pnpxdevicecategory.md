---
description: Especifica a categoria PnP-X à qual o dispositivo pertence. Mais de uma categoria pode ser especificada.
ms.assetid: 1ca46000-4700-4326-8f49-1b9a22d45bfa
title: Elemento PnPXDeviceCategory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42a34a3f63333a2d33266991c0e028e7d42a7244c962617974c9cc15e290d03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897356"
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
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define o fabricante e os metadados do modelo para o dispositivo a ser implementado.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os dispositivos também podem especificar uma subcategoria de dispositivo para uma categoria de dispositivo mais descritiva. Por exemplo, "Phones.WindowsMobile Cameras.DigitalStillCamera MediaDevices.MusicPlayer" identifica um dispositivo que é um dispositivo Microsoft Windows Mobile com uma câmera e um player de música. A categoria de dispositivo principal para esse dispositivo seria "Telefones".

Para especificar mais de uma categoria de dispositivo, separe as categorias com um espaço. Por exemplo, "Impressoras Armazenamento" identifica um dispositivo com uma categoria primária de "Impressoras" e uma categoria secundária de "Armazenamento".

Se um **elemento PnPXDeviceCategory** estiver presente, pelo menos um elemento hospedado deverá conter elementos [**PnPXHardwareId**](pnpxhardwareid.md) e [**PnPXCompatibleId.**](pnpxcompatibleid.md) [](hosted.md) Da mesma forma, se os elementos **PnPXHardwareId** e  **PnPXCompatibleId** estão presentes em um elemento hospedado, pelo menos um elemento **PnPXDeviceCategory** deve estar presente dentro do elemento [**thisModelMetadata.**](thismodelmetadata.md)

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




