---
description: Cria um ponto de referência de um sistema virtual.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Método CreateReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014474"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método CreateReferencePoint da \_ classe VirtualSystemReferencePointService Msvm

Cria um ponto de referência de um sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSystem* \[ no\]
</dt> <dd>

Um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que faz referência ao sistema virtual afetado.

</dd> <dt>

*ReferencePointSettings* \[ no\]
</dt> <dd>

Contém as configurações de parâmetro.

</dd> <dt>

*ReferencePointType* \[ no\]
</dt> <dd>

Tipo de ponto de referência solicitado:

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (0)


</dt> <dd>

Com base no rastreamento de log de réplica do Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (1)


</dt> <dd>

Com base em Controle de Alterações resilientes de discos virtuais.

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[ entrada, saída\]
</dt> <dd>

Ponto de referência do sistema virtual resultante

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado. Nesse caso, a instância da classe [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o novo ponto de referência do sistema virtual é apresentada por meio da Associação de [**\_ AffectedJobElement do CIM**](cim-affectedjobelement.md) com o valor da propriedade **afetou** que se refere à nova instância da classe **Msvm \_ VirtualSystemReferencePoint** que representa o ponto de referência do sistema virtual e o valor do **ElementEffects** definido como 5 (criar).

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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




