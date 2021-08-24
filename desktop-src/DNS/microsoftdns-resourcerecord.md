---
title: MicrosoftDNS_ResourceRecord classe
description: A classe ResourceRecord do MicrosoftDNS \_ representa as propriedades gerais de um DNS RR. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- dns MicrosoftDNS_ResourceRecord classe
- MicrosoftDNS_ResourceRecord classe DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874796"
---
# <a name="microsoftdns_resourcerecord-class"></a>Classe ResourceRecord do MicrosoftDNS \_

A **classe \_ ResourceRecord do MicrosoftDNS** representa as propriedades gerais de um DNS RR.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Membros

A **classe \_ ResourceRecord do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ ResourceRecord do MicrosoftDNS** tem esses métodos.



| Método                                   | Descrição                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analisará o RR na cadeia de caracteres TextRepresentation e, com os Nomes de Servidor DNS e Contêiner de entrada, definirá e insinuou um objeto ResourceRecord. O método retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: nenhum<br/> |
| **GetObjectByTextRepresentation**        | Recupera uma instância existente da subclasse MicrosoftDns ResourceRecord, representada pela cadeia de caracteres TextRepresentation juntamente com o Servidor DNS e o Nome \_ do Contêiner. <br/> Qualificadores: nenhum<br/>                                                        |



 

### <a name="properties"></a>Propriedades

A **classe \_ ResourceRecord do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Containername**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o nome do Contêiner para a instância Zone, Cache ou RootHints que contém o RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o FQDN ou o endereço IP do Servidor DNS que contém o RR.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representa o FQDN do domínio que contém o RR. Essa propriedade pode conter as cadeias de caracteres \\ .. Cache \\ ou \\ .. RootHints \\ se o cache interno ou RootHints contêm o RR, respectivamente.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do proprietário para a RR.

</dd> <dt>

**RecordClass=1**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**Windows Server 2003: **

Essa cadeia de caracteres representa a classe do Registro de Recurso. Os valores válidos incluem:

1: IN (Internet)

2: CS (CSNET)

3: CH (CHAOS)

4: HS (Hesiod)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados de registro de recurso.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representação de texto de toda a RR.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que a RR foi atualizada pela última vez, expressa em horas decorridos desde 1º de janeiro de 1601, Horário De Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, em que o RR pode ser armazenado em cache por um resolvedor [*de*](r-gly.md)DNS .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método CreateInstanceFromTextRepresentation da classe ResourceRecord do MicrosoftDNS \_**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Método GetObjectByTextRepresentation da classe ResourceRecord do MicrosoftDNS \_**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





