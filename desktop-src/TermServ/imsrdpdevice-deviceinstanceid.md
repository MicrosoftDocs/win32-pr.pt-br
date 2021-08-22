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
ms.openlocfilehash: 74fd93b775d3fd239435a984cf0f0b7518558f3f57e92525365764da580f499c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606812"
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

 

 





