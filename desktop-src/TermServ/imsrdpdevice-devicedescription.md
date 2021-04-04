---
title: Propriedade IMsRdpDevice DeviceDescription
description: Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceDescription
- Propriedade DeviceDescription Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice, Propriedade DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085867"
---
# <a name="imsrdpdevicedevicedescription-property"></a>IMsRdpDevice: Propriedade eviceDescription de:D

Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a>Valor da propriedade

A descrição do dispositivo.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, **S \_ OK** será retornado. Qualquer outro valor **HRESULT** indica que a chamada falhou.

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

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





