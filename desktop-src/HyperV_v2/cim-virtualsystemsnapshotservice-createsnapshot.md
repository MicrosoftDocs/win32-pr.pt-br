---
description: Cria um instantâneo de um sistema virtual.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Método CreateSnapshot da CIM_VirtualSystemSnapshotService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee1a2e66745ceac50cc00ba6e625a171f18c7d2b54d4e51af2c86f6711675ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532746"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a>Método CreateSnapshot da classe CIM \_ VirtualSystemSnapshotService

Cria um instantâneo de um sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSystem* \[ Em\]
</dt> <dd>

Uma [**referência do Cim \_ ComputerSystem**](cim-computersystem.md) ao sistema virtual afetado.

</dd> <dt>

*SnapshotSettings* \[ Em\]
</dt> <dd>

Configurações de parâmetro.

</dd> <dt>

*SnapshotType* \[ Em\]
</dt> <dd>

Tipo de instantâneo solicitado:

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantâneo completo** (2)


</dt> <dd>

Instantâneo completo do sistema virtual.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantâneo de disco** (3)


</dt> <dd>

Instantâneo de discos do sistema virtual.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do** fornecedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Uma [**referência CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) ao instantâneo do sistema virtual resultante.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for de execução longa, opcionalmente, um trabalho poderá ser retornado. Nesse caso, a instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa o novo instantâneo do sistema virtual é apresentada por meio da associação [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) com o valor da propriedade **AffectedElement** que se refere à nova instância da classe **CIM \_ VirtualSystemSettingData** que representa o instantâneo do sistema virtual e o valor do **ElementEffects definido como** 5 (Criar).

> [!Note]  
> Esse parâmetro foi lido/escrito Windows 8.1.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempoout** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**Estado inválido** (5)
</dt> <dt>

**Tipo inválido** (6)
</dt> <dt>

**DMTF Reservado** (..)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Método Reservado** (4097..32767)
</dt> <dt>

**Específico do** fornecedor (32768..65535)
</dt> </dl>

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

[**CIM \_ VirtualSystemSnapshotService**](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




