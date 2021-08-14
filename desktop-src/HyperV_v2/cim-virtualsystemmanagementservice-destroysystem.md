---
description: Destrói um sistema virtual.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Método DestroySystem da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa7bf479e1e861e8425376fa0ebb610cd0b728cc9f02ba80acc9c1faa284fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980546"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método DestroySystem da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM

Destrói um sistema virtual.

O sistema virtual referenciado é destruído, incluindo todos os elementos com escopo definido por ele. Os recursos virtuais são retornados para seus pools de recursos, o que pode implicar a destruição desses recursos (dependente de implementação). Se o sistema virtual estiver ativo quando a operação for chamada, ele será desativado primeiro e depois destruído. Se os instantâneos foram criados a partir do sistema virtual, eles também são destruídos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSystem* \[ no\]
</dt> <dd>

Referência a uma instância da classe [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o sistema de computador virtual a ser destruído.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

**Estado inválido** (5)
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

 

 




