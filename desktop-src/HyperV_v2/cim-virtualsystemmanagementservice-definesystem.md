---
description: Define um sistema virtual.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Método DefineSystem da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785459"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método DefineSystem da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM

Define um sistema virtual.

A entrada que não está completamente especificada pode ser preenchida com valores padrão.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SystemSettings* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que é usada para definir os atributos do sistema virtual a ser criado.

</dd> <dt>

*ResourceSettings* \[ no\]
</dt> <dd>

Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve os aspectos virtuais de um recurso virtual a ser criado no escopo do novo sistema virtual.

</dd> <dt>

*ReferenceConfiguration* \[ no\]
</dt> <dd>

Referência a uma instância de objeto [**CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) que é o objeto de nível superior de uma configuração de sistema virtual de referência. A configuração de referência será usada para complementar a configuração do novo sistema virtual se os parâmetros *SystemSettings* e *ResourceSettings* não fornecerem as respectivas informações.

</dd> <dt>

*ResultingSystem* \[ fora\]
</dt> <dd>

Se um sistema de computador virtual for definido com êxito, uma referência a uma instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o sistema de computador virtual recém-definido é retornado.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado. Nesse caso, a instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o novo sistema virtual é apresentada por meio [**de \_ AffectedJobElement de CIM**](cim-affectedjobelement.md) de associação com a propriedade **afetoed** fazendo referência à nova instância da classe **CIM \_ ComputerSystem** e da propriedade **ElementEffects** definida como 5 (Create).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

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

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




