---
description: O método QuiesceDevice foi preterido em vez do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Método QuiesceDevice da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7becb86f19c245488d779e1b26ab5321ba3f2aa0ac3c7811d96f9d1cb8a5dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995688"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Método QuiesceDevice da classe \_ LogicalDevice cim

O **método QuiesceDevice** foi preterido em vez do método **RequestStateChange** mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.

## <a name="syntax"></a>Sintaxe


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Quiesce* \[ Em\]
</dt> <dd>

Se definido como **TRUE,** corretamente interromperá todas as atividades, se **FALSE retomar** a atividade.

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

 

 




