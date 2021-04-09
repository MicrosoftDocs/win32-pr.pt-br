---
description: O histórico recente de alterações nos dados de encaminhamento de um computador de destino.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Classe TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089682"
---
# <a name="targetforwardinghistory-class"></a>Classe TargetForwardingHistory

O histórico recente de alterações nos dados de encaminhamento de um computador de destino.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Membros

A classe **TargetForwardingHistory** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **TargetForwardingHistory** tem essas propriedades.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações do ponto de extremidade do servidor do coletor. Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* .

</dd> <dt>

**Computador**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O nome do computador de destino.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O carimbo de data/hora que indica quando a conexão foi estabelecida para os dados de encaminhamento.

</dd> <dt>

**Destino**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O destino dos dados de encaminhamento, como um nome de arquivo.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O formato usado para gerar o destino dos dados de encaminhamento.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O carimbo de data/hora que indica quando a conexão foi desconectada.

</dd> <dt>

**Erro**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Uma mensagem de erro que descreve um erro encontrado. Essa propriedade estará vazia se nenhum erro for encontrado.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O tipo de arquivo que contém os dados de encaminhamento, como ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações do ponto de extremidade do computador de destino, no formato legível por humanos. Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* . Por exemplo, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O SMBIOS **GUID** do computador de destino.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O endereço MAC do computador de destino.

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Carimbo de data/hora de quando essa alteração de estado foi registrada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor WMI do coletor de eventos de inicialização](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

