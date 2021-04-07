---
title: Classe MicrosoftDNS_ResourceRecord
description: A \_ classe MicrosoftDNS ResourceRecord representa as propriedades gerais de um RR DNS. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord de classe de DNS
- MicrosoftDNS_ResourceRecord de classe de DNS, descrita
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
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918603"
---
# <a name="microsoftdns_resourcerecord-class"></a>\_Classe MicrosoftDNS ResourceRecord

A classe **MicrosoftDNS \_ ResourceRecord** representa as propriedades gerais de um RR DNS.

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

A classe **MicrosoftDNS \_ ResourceRecord** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ ResourceRecord** tem esses métodos.



| Método                                   | Descrição                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analisa o RR na cadeia de caracteres textrepresentation e com o servidor DNS de entrada e os nomes de contêiner, define e instancia um objeto ResourceRecord. O método retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: nenhum<br/> |
| **GetObjectByTextRepresentation**        | Recupera uma instância existente da subclasse MicrosoftDns \_ ResourceRecord, representada pela cadeia de caracteres Textrepresentation, junto com o servidor DNS e o nome do contêiner. <br/> Qualificadores: nenhum<br/>                                                        |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ ResourceRecord** tem essas propriedades.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o nome do contêiner para a zona, o cache ou a instância de RootHints que contém o RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o FQDN ou o endereço IP do servidor DNS que contém o RR.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representa o FQDN do domínio que contém o RR. Essa propriedade pode conter as cadeias de caracteres \\ .. Cache \\ ou \\ .. RootHints \\ se o cache interno ou RootHints contiver o RR, respectivamente.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do proprietário do RR.

</dd> <dt>

**RecordClass = 1**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

* * Windows Server 2003: * *

Essa cadeia de caracteres representa a classe do registro de recurso. Os valores válidos incluem:

1: IN (Internet)

2: CS (CSNET)

3: CH (CAOS)

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

**Textrepresentation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representação de texto de todo o RR.

</dd> <dt>

**Estampa**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o RR foi atualizado pela última vez, expresso em horas decorridas desde 1º de janeiro de 1601, Greenwich Mean Time (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, que o RR pode ser armazenado em cache por um [*resolvedor*](r-gly.md)de DNS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





