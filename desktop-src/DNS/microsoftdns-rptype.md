---
title: Classe MicrosoftDNS_RPType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de RP (pessoa responsável).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType de classe de DNS
- MicrosoftDNS_RPType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aae8686016d26cb9007b21a06c125d56ed5207f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824504"
---
# <a name="microsoftdns_rptype-class"></a>\_Classe MicrosoftDNS RPType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de RP (pessoa responsável).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ RPType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ RPType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um tipo de RR de RP com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/pessoa responsável, a classe (padrão = IN), o valor de vida útil e os nomes de domínio para a caixa de correio e os locais RR do TXT da pessoa. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Esse método atualiza o TTL, a caixa de correio RP e o nome de domínio TXT para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                                  |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ RPType** tem essas propriedades.

<dl> <dt>

**RPMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica a caixa de correio da pessoa responsável.

</dd> <dt>

**TXTDomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN para o qual os registros de recurso TXT existem.

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

[**Método CreateInstanceFromPropertyData da \_ classe RPType MicrosoftDNS**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ RPType**](microsoftdns-rptype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





