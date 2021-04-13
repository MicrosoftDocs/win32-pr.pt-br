---
title: Propriedade IMsRdpDeviceCollection DeviceByIndex
description: Recupera o dispositivo no índice especificado.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DeviceByIndex
- Propriedade DeviceByIndex Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, Propriedade DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456001"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a>IMsRdpDeviceCollection: Propriedade eviceByIndex de:D

Recupera o dispositivo no índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro de interface [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, **S \_ OK** será retornado. Qualquer outro valor **HRESULT** indica que a chamada falhou.

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

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





