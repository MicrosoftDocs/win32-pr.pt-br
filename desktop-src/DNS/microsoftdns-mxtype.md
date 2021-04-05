---
title: Classe MicrosoftDNS_MXType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um RR de troca de mensagens (Mr).
ms.assetid: 7c147628-5bda-48dd-beb4-e630d1886da8
keywords:
- MicrosoftDNS_MXType de classe de DNS
- MicrosoftDNS_MXType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
- MicrosoftDNS_MXType.Modify
- MicrosoftDNS_MXType.Preference
- MicrosoftDNS_MXType.MailExchange
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652743178b71b2f9fed296ecfa4427f85b5cf1c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918451"
---
# <a name="microsoftdns_mxtype-class"></a>\_Classe MicrosoftDNS MXType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um RR de troca de mensagens (Mr).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_MXType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string MailExchange;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ MXType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ MXType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um tipo MX de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil, a preferência de registro e o nome do host que está disposto a ser uma troca de email. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o TTL, a preferência e a troca de email para os valores especificados como os parâmetros de entrada deste método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                         |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ MXType** tem essas propriedades.

<dl> <dt>

**MailExchange**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica um host que está disposto a atuar como uma troca de email para o nome do proprietário.

</dd> <dt>

**Preferência**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Preferência dada a esse RR entre outros no mesmo proprietário. Os valores mais baixos são preferenciais.

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

[**Método CreateInstanceFromPropertyData da \_ classe MXType MicrosoftDNS**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ MXType**](microsoftdns-mxtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





