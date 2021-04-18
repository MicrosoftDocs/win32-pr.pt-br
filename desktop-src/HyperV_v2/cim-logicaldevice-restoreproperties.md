---
description: Solicita que o dispositivo restabeleça a configuração, a configuração e/ou as informações de estado de um repositório de backup.
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: Método restoreproperties da classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811880"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>Método restoreproperties da classe CIM \_ LogicalDevice

Solicita que o dispositivo restabeleça a configuração, a configuração e/ou as informações de estado de um repositório de backup. A intenção é capturar essas informações em um momento anterior (por meio do método SaveProperties) e usá-las para retornar um dispositivo para essa "condição" anterior. Esse método pode não ter suporte de todos os dispositivos. O método deve retornar 0 se for bem-sucedido, 1 se a solicitação não tiver suporte e algum outro valor se ocorrer algum outro erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado, usando um qualificador ValueMap no método. As cadeias de caracteres para as quais o conteúdo de ValueMap são ' convertidas ' também podem ser especificadas na subclasse como um qualificador de matriz de valores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

 

 




