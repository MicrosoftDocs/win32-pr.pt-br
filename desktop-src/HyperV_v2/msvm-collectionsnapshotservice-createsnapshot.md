---
description: Cria um instantâneo de uma coleção de sistemas virtuais.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Método createsnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 251213d0ff7a98d922a4dec761252479f911e66e2304596a97858fe0b7dc5fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426906"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método createsnapshot da classe Msvm \_ CollectionSnapshotService

Cria um instantâneo de uma coleção de sistemas virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Coleção* \[ de no\]
</dt> <dd>

Referência a um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) que descreve a coleção de sistema virtual afetada.

</dd> <dt>

*SnapshotSettings* \[ no\]
</dt> <dd>

Contém as configurações de parâmetro.

</dd> <dt>

*Instantâneotype* \[ no\]
</dt> <dd>

Tipo de instantâneo solicitado:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Instantâneo padrão** (1)


</dt> <dd>

Instantâneo padrão do sistema virtual.

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Instantâneo de recuperação** (2)


</dt> <dd>

Instantâneo para cenários de recuperação, incluindo replicação de failover e backup.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshotCollection* \[ entrada, saída\]
</dt> <dd>

Em caso de sucesso, retorna uma referência de [**\_ coleção CIM**](cim-collection.md) que contém o instantâneo do sistema virtual.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0 (completo) ou 4096 (trabalho iniciado); caso contrário, retornará um erro.

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

**Tipo inválido** (6)
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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




