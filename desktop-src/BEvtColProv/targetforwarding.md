---
description: Recupera dados de encaminhamento de um computador de destino.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Classe TargetForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: a6025089d069504889d7b97d87a73b167746c3e594013acf58f0ed615162f787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529686"
---
# <a name="targetforwarding-class"></a>Classe TargetForwarding

Recupera dados de encaminhamento de um computador de destino.

> [!Note]  
> Um computador de destino pode ter vários encaminhadores configurados.

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a>Membros

A **classe TargetForwarding** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe TargetForwarding** tem essas propriedades.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações de ponto de extremidade do servidor coletor. Essa propriedade é formatada como um *host*: cadeia *de caracteres de* porta.

</dd> <dt>

**Computador**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O nome do computador de destino.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O timestamp que indica quando a conexão foi estabelecida para os dados de encaminhamento.

</dd> <dt>

**Destino**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O destino dos dados de encaminhamento, como um nome de arquivo.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O formato usado para gerar o destino dos dados de encaminhamento.

</dd> <dt>

**Erro**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Uma mensagem de erro que descreve um erro encontrado. Essa propriedade será vazia se nenhum erro for encontrado.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **corrigidos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O tipo de arquivo que contém os dados de encaminhamento, como ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações de ponto de extremidade do computador de destino, em formato acessível por humanos. Essa propriedade é formatada como um *host*: cadeia *de caracteres de* porta. Por exemplo, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O **GUID** SMBIOS do computador de destino.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O endereço MAC do computador de destino.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor WMI do Coletor de Eventos de Inicialização](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

