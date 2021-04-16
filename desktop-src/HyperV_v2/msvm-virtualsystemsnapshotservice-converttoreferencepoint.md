---
description: Converta um instantâneo do sistema virtual existente em um ponto de referência. O instantâneo é excluído como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Método ConvertToReferencePoint da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768504"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Método ConvertToReferencePoint da \_ classe VirtualSystemSnapshotService Msvm

Converta um instantâneo do sistema virtual existente em um ponto de referência. O instantâneo é excluído como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSnapshot* \[ no\]
</dt> <dd>

Referência ao instantâneo do sistema virtual afetado.

</dd> <dt>

*ReferencePointSettings* \[ no\]
</dt> <dd>

Configurações de parâmetro.

</dd> <dt>

*ResultingReferencePoint* \[ entrada, saída\]
</dt> <dd>

Ponto de referência do sistema virtual resultante

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retorna um dos seguintes valores:

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




