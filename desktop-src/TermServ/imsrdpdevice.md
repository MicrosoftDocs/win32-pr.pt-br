---
title: Interface IMsRdpDevice
description: Contém informações sobre um objeto de dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice
- Serviços de Área de Trabalho Remota da interface IMsRdpDevice, descrita
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033086"
---
# <a name="imsrdpdevice-interface"></a>Interface IMsRdpDevice

Contém informações sobre um objeto de dispositivo.

## <a name="members"></a>Membros

A interface **IMsRdpDevice** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDevice** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpDevice** tem essas propriedades.



| Propriedade                                                               | Tipo de acesso           | Descrição                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Somente leitura<br/>  | Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Somente leitura<br/>  | Recupera o identificador da instância de dispositivo do dispositivo.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Somente leitura<br/>  | Recupera o nome de exibição do dispositivo.<br/>                                                         |
| [**De redirecionamento**](imsrdpdevice-redirectionstate.md)<br/>   | Leitura/gravação<br/> | Indica o estado de redirecionamento do dispositivo.<br/>                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

