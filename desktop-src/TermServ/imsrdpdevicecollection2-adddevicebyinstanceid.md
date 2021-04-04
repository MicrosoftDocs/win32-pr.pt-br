---
title: Método IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Adiciona um dispositivo não listado à coleção de dispositivos.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddDeviceByInstanceId
- Método AddDeviceByInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection2, método AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008884"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>Método IMsRdpDeviceCollection2:: AddDeviceByInstanceId

Adiciona um dispositivo não listado à coleção de dispositivos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Um valor da enumeração [**RedirectDeviceType**](redirectdevicetype.md) que especifica o tipo de dispositivo que está sendo adicionado.

</dd> <dt>

*InstanceId* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O identificador de instância do dispositivo a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





