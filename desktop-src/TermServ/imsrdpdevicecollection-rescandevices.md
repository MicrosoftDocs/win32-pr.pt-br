---
title: Método IMsRdpDeviceCollection RescanDevices
description: Atualiza a lista de objetos na coleção. | Método IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RescanDevices
- Método RescanDevices Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection, método RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959236"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>Método IMsRdpDeviceCollection:: RescanDevices

Atualiza a lista de objetos na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vboolDynRedir* \[ no\]
</dt> <dd>

O estado de redirecionamento padrão que será aplicado a quaisquer unidades ou dispositivos descobertos recentemente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





