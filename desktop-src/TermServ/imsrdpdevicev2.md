---
title: Interface IMsRdpDeviceV2
description: Contém informações sobre um objeto de dispositivo. Esse é um aprimoramento da interface IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpDeviceV2 Serviços de Área de Trabalho Remota
- Interface IMsRdpDeviceV2 Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca125024592851b260fb8e4c1f43c7621d4897fec0fc19dfc80d18278e09cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000746"
---
# <a name="imsrdpdevicev2-interface"></a>Interface IMsRdpDeviceV2

Contém informações sobre um objeto de dispositivo. Esse é um aprimoramento da interface [**IMsRdpDevice.**](imsrdpdevice.md)

## <a name="members"></a>Membros

A interface **IMsRdpDeviceV2** herda [**de IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpDeviceV2** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Somente leitura<br/> | Contém o GUID da classe de instalação do configuration manager para o dispositivo.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Somente leitura<br/> | Contém a instância de dispositivo do configuration Manager do dispositivo.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Somente leitura<br/> | Contém o texto do dispositivo.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Somente leitura<br/> | Contém um campo de bits que representa um mapa de letras de unidade contidas no dispositivo.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Somente leitura<br/> | Especifica se o dispositivo é um dispositivo composto.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Somente leitura<br/> | Especifica se o dispositivo é opcional para redirecionamento de USB.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Somente leitura<br/> | Especifica se o dispositivo é para redirecionamento DE USB.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 com SP1<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2 com SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





