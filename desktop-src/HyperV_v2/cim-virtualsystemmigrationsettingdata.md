---
description: Define as configurações para a migração do sistema virtual que é gerenciada por uma instância da classe CIM \_ VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24a48877a4195d17398457912314186d0220ace8016a4c9cc3edd3e06c378ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950665"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>Classe CIM \_ VirtualSystemMigrationSettingData

Define as configurações para a migração do sistema virtual que é gerenciada por uma instância da [**classe CIM \_ VirtualSystemMigrationService.**](cim-virtualsystemmigrationservice.md)

## <a name="syntax"></a>Sintaxe

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ VirtualSystemMigrationSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ VirtualSystemMigrationSettingData** tem essas propriedades.

<dl> <dt>

**Largura de banda**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Medidor**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

A largura de banda atribuída ou solicitada para uma operação de migração do sistema virtual. "0" é a largura de banda padrão para solicitações de migração.

As **propriedades Largura** de Banda e Prioridade podem ser usadas em conjunto.  Os processos de migração que têm os valores **de Prioridade** iguais mais altos compartilham a largura de banda disponível com base na largura de banda solicitada. Se nem toda a largura de banda for consumida por esse conjunto de processos, os processos de migração com os próximos valores de **Prioridade** iguais menores compartilharão a largura de banda restante. Se mais largura de banda permanecer, os processos de migração com os próximos valores **de Prioridade** iguais menores serão considerados.

A unidade usada na **propriedade Bandwidth** é especificada pelo valor da propriedade **BandwidthUnit.**

Se o valor da propriedade **BandwidthUnit** for "percent", as seguintes regras se aplicarão:

-   O valor da propriedade **Bandwidth** deve estar entre "0" e "100", com valores mais altos indicando uma largura de banda maior.
-   Um valor de "100" indica toda a largura de banda disponível para executar operações de migração do sistema virtual.
-   Valores entre "1" e "100" se correlacionam linearmente com o intervalo de largura de banda disponível. Por exemplo, um valor de 50 solicita metade da largura de banda disponível.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Largura de** banda "), **IsPUnit**
</dt> </dl>

A unidade usada pela propriedade **Bandwidth.** O valor dessa propriedade deve ser um valor legal do qualificador unidades programáticas definido no Apêndice C.1 de DSP0004 V2.4 ou posterior.

> [!Note]  
> Perfis como DMTF DSP1081 definem como os clientes podem descobrir o conjunto de unidades com suporte por uma implementação e intervalos e incrementos para valores da propriedade **Bandwidth.**

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de operação de migração a ser realizada.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Ao vivo** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

**Retomar** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Reiniciar** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")
</dt> </dl>

O tipo de transporte a ser aplicado se o valor de **TransportType** for "1" (outro).

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A importância relativa da migração que a implementação de migração do sistema virtual pode usar para ordenar ou atribuir preferência entre várias solicitações de migração pendentes. Quanto menor o valor, maior a prioridade. "0" é a largura de banda padrão para solicitações de migração.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

O tipo de transporte a ser aplicado a uma operação de migração do sistema virtual.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor Reservado** (32768..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> </dl>

 

