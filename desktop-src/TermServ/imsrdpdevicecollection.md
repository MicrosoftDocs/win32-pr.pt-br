---
title: Interface IMsRdpDeviceCollection
description: Representa uma coleção de objetos de dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpDeviceCollection, descrita
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5f7008b0b524150cd106b9bbe97d21a8de890773d8b0b461a6ae3045e847a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000736"
---
# <a name="imsrdpdevicecollection-interface"></a>Interface IMsRdpDeviceCollection

Representa uma coleção de objetos de dispositivo.

## <a name="members"></a>Membros

A interface **IMsRdpDeviceCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDeviceCollection** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IMsRdpDeviceCollection** tem esses métodos.



| Método                                                        | Descrição                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | Atualiza a lista de objetos na coleção.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IMsRdpDeviceCollection** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | Somente leitura<br/> | Recupera o dispositivo com o identificador especificado.<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Somente leitura<br/> | Recupera o dispositivo no índice especificado.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Somente leitura<br/> | Recupera a contagem de objetos na coleção.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

