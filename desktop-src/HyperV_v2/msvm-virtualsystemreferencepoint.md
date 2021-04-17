---
description: Representa um ponto de referência para um sistema virtual.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Classe Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105755991"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a>\_Classe Msvm VirtualSystemReferencePoint

Representa um ponto de referência para um sistema virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemReferencePoint** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemReferencePoint** tem essas propriedades.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O nível de consistência do ponto de referência.

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)


</dt> <dd>

O ponto de referência indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)


</dt> <dd>

O ponto de referência indica um ponto no tempo em que o sistema virtual estava em estado de falha consistente.

</dd> </dl>

</dd> <dt>

**HasAssociatedData**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Defina como **true** se o ponto de referência tiver dados associados. Isso é válido somente para pontos de referência baseados em log. Para pontos de referência baseados em RCT, **HasAssociatedData** é definido como **false**. Para pontos de referência baseados em log, uma vez que o log é Descartado, o **HasAssociatedData** se torna **falso**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificação exclusiva de um objeto de ponto de referência.

</dd> <dt>

**ReferencePointType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica o tipo do ponto de referência.

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Baseado em log** (1)


</dt> <dd>

Rastreamento de log de réplica do Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Baseado em RCT** (2)


</dt> <dd>

Com base em Controle de Alterações resilientes de discos virtuais.

</dd> </dl>

</dd> <dt>

**ResilientChangeTrackingIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de IDs de RCT correspondente aos discos virtuais da VM no momento em que esse ponto de referência foi criado. Este campo é válido somente para pontos de referência baseados em RCT.

</dd> <dt>

**VirtualDiskIdentifiers**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de IDs de instância do WMI correspondente aos discos virtuais da VM no momento em que esse ponto de referência foi criado. Esses discos virtuais têm IDs RCT associadas a eles.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Nome**")
</dt> </dl>

O nome do [**sistema de \_ ComputerSystem CIM**](cim-computersystem.md) ao qual este ponto de referência pertence

</dd> </dl>

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

[**\_Managedelement do CIM**](cim-managedelement.md)
</dt> </dl>

 

