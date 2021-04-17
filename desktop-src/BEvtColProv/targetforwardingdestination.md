---
description: Os destinos conhecidos que contêm os dados coletados. Disponível somente se o coletor estiver em execução com o log de status habilitado.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Classe TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456893"
---
# <a name="targetforwardingdestination-class"></a>Classe TargetForwardingDestination

Os destinos conhecidos que contêm os dados coletados. Disponível somente se o coletor estiver em execução com o log de status habilitado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

A classe **TargetForwardingDestination** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **TargetForwardingDestination** tem essas propriedades.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações de host: porta do ponto de extremidade no lado do coletor.

</dd> <dt>

**Computador**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome do computador de destino, conforme determinado pelo coletor de acordo com sua configuração.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Carimbo de data/hora de quando a conexão foi estabelecida.

</dd> <dt>

**Destino**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destino dos dados. O significado depende do tipo de encaminhador. Pode ser um nome de arquivo ou alguma outra identificação.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Padrão usado para gerar o destino dos dados. O significado depende do tipo de encaminhador e da configuração. Para um destino fixo, seria o mesmo que o próprio destino. Para o destino com rotação dos arquivos, conterá os caracteres padrão que serão substituídos pelo índice real no destino.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Carimbo de data/hora de quando a conexão foi descartada.

</dd> <dt>

**Erro**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Mensagem de erro se um erro foi encontrado. Caso contrário, estará vazio.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**fixo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Tipo do encaminhador (como ' ETL ').

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

As informações do ponto de extremidade do computador de destino, no formato legível por humanos. Essa propriedade é formatada como uma cadeia de caracteres de *host*:*porta* . Por exemplo, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O SMBIOS GUID do computador de destino (se conhecido).

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

O endereço MAC do computador de destino (se conhecido).

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



 

