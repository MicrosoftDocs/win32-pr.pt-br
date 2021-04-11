---
description: O método QuiesceDevice foi preterido no lugar do método RequestStateChange mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.
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
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297210"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Método QuiesceDevice da classe CIM \_ LogicalDevice

O método **QuiesceDevice** foi preterido no lugar do método **RequestStateChange** mais geral que se sobrepõe diretamente à funcionalidade fornecida por esse método.

## <a name="syntax"></a>Sintaxe


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desativar* \[ no\]
</dt> <dd>

Se definido como **true** , interrompa corretamente todas as atividades, se **false** retomar a atividade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




