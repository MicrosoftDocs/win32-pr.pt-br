---
title: Propriedade IMsRdpDevice DeviceInstanceId
description: Recupera o identificador da instância de dispositivo do dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceInstanceId
- Propriedade DeviceInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpDevice
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice, Propriedade DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919204"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a>IMsRdpDevice: Propriedade eviceInstanceId de:D

Recupera o identificador da instância de dispositivo do dispositivo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a>Valor da propriedade

O identificador da instância do dispositivo.

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

 

 





