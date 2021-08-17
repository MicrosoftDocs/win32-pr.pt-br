---
description: Cria um ponto de referência de uma coleção de sistemas virtuais.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Método CreateReferencePoint da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e1745a02b643f035dd46d82e1686a8f5075157a7f749a701865028f3a7db162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994797"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método CreateReferencePoint da classe Msvm \_ CollectionReferencePointService

Cria um ponto de referência de uma coleção de sistemas virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Coleção* \[ Em\]
</dt> <dd>

Referência à coleção do sistema virtual afetada.

</dd> <dt>

*ReferencePointSettings* \[ Em\]
</dt> <dd>

Configurações de parâmetro.

</dd> <dt>

*ReferencePointType* \[ Em\]
</dt> <dd>

Indica o tipo do ponto de referência.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (1)


</dt> <dd>

Acompanhamento de log de réplica do Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (2)


</dt> <dd>

Com base na Controle de Alterações de discos virtuais.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do** fornecedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingReferencePointCollection* \[ in, out\]
</dt> <dd>

Ponto de referência resultante de uma coleção de sistema virtual.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for de execução longa, opcionalmente, um trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, retornará 0 (sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.

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
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




