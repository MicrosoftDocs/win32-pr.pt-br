---
title: Propriedade IMsRdpDeviceCollection DeviceById
description: Recupera o dispositivo com o identificador especificado.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Propriedade DeviceById Serviços de Área de Trabalho Remota
- A propriedade DeviceById Serviços de Área de Trabalho Remota , interface IMsRdpDeviceCollection
- Interface IMsRdpDeviceCollection Serviços de Área de Trabalho Remota propriedade DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fd3fd67afebb4c853d5db71a429dc99f61d3bbc178e9ddd73b91284893108b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940978"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a>Propriedade IMsRdpDeviceCollection::D eviceById

Recupera o dispositivo com o identificador especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro de interface [**IMsRdpDevice.**](imsrdpdevice.md)

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection é definido como 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





