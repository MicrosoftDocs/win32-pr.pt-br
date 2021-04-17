---
description: Gerencia os dispositivos atribuíveis em um sistema de computador host.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Classe Msvm_AssignableDeviceService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759875"
---
# <a name="msvm_assignabledeviceservice-class"></a>\_Classe Msvm AssignableDeviceService

Gerencia os dispositivos atribuíveis em um sistema de computador host.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ AssignableDeviceService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Msvm \_ AssignableDeviceService** tem esses métodos.



| Método                                                                                    | Descrição                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**DismountAssignableDevice**](msvm-assignabledeviceservice-dismountassignabledevice.md) | Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.<br/>                      |
| [**MountAssignableDevice**](msvm-assignabledeviceservice-mountassignabledevice.md)       | Monta o dispositivo PCI especificado para que ele possa ser usado pelo sistema de computador host.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




