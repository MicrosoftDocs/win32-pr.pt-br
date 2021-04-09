---
title: Classe MicrosoftDNS_Statistic
description: A \_ classe de estatística MicrosoftDNS representa uma única estatística de servidor DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic de classe de DNS
- MicrosoftDNS_Statistic de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009644"
---
# <a name="microsoftdns_statistic-class"></a>\_Classe de estatística MicrosoftDNS

A classe de **\_ estatística MicrosoftDNS** representa uma única estatística de servidor DNS.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>Membros

A classe de **\_ estatística MicrosoftDNS** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ estatística MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representação numérica de **CollectionName**.

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da coleção à qual a estatística pertence.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o FQDN ou o endereço IP do servidor DNS que contém a estatística.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da estatística.

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor da cadeia de caracteres da estatística, usado somente quando o valor da estatística não é representado como um DWORD.

</dd> <dt>

**Valor**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor numérico da estatística, representado como um DWORD.

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

[\_Estatísticacollection de MicrosoftDNS](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





