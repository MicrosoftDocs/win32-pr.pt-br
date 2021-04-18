---
description: Injeta uma interrupção não mascarável na máquina virtual.
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: 'Método Msvm_ComputerSystem:: InjectNonMaskableInterrupt'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5798079a8866d9fb67356adff43c0ac1e993e6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778755"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a>\_Método Msvm ComputerSystem:: InjectNonMaskableInterrupt

Injeta uma interrupção não mascarável na máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) para acompanhar o status da injeção de interrupção. Essa referência poderá ser **nula** se a tarefa for concluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Acesso negado** (32769)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

