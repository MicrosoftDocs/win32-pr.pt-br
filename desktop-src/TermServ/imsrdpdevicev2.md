---
title: Interface IMsRdpDeviceV2
description: Contém informações sobre um objeto de dispositivo. Esse é um aprimoramento da interface IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota da interface IMsRdpDeviceV2, descrita
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
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757933"
---
# <a name="imsrdpdevicev2-interface"></a>Interface IMsRdpDeviceV2

Contém informações sobre um objeto de dispositivo. Esse é um aprimoramento da interface [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="members"></a>Membros

A interface **IMsRdpDeviceV2** herda de [**IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpDeviceV2** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Somente leitura<br/> | Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Somente leitura<br/> | Contém a instância de dispositivo do Configuration Manager do dispositivo.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Somente leitura<br/> | Contém o texto do dispositivo.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Somente leitura<br/> | Contém um campo de bits que representa um mapa de letras de unidade contidas no dispositivo.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Somente leitura<br/> | Especifica se o dispositivo é um dispositivo composto.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Somente leitura<br/> | Especifica se o dispositivo é opcional para o redirecionamento de USB.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Somente leitura<br/> | Especifica se o dispositivo é para o redirecionamento de USB.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 com SP1<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2 com SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





