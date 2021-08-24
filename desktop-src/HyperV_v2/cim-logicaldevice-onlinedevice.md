---
description: O método OnlineDevice foi preterido em vez do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Método OnlineDevice da CIM_LogicalDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f34d08ad72bd04cd94e35ac229fde82ca4847ec13410e35d57d0de0778d50af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695506"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Método OnlineDevice da classe \_ LogicalDevice cim

O **método OnlineDevice** foi preterido em vez do método **RequestStateChange** mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.

## <a name="syntax"></a>Sintaxe


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Online* \[ Em\]
</dt> <dd>

Se **TRUE**, leve o dispositivo online, se **FALSE,** para que o dispositivo seja offline.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




