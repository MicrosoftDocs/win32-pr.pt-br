---
title: Classe MicrosoftDNS_MDType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de agente de email para o domínio (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType de classe de DNS
- MicrosoftDNS_MDType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824390"
---
# <a name="microsoftdns_mdtype-class"></a>\_Classe MicrosoftDNS MDType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de agente de email para o domínio (MD).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ MDType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ MDType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancia um registro de recurso de DNS MD com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário do domínio, a classe (padrão = IN), o valor de vida útil e o host do agente de email. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o TTL e o host MD para os valores especificados como os parâmetros de entrada deste método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                                 |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ MDType** tem essas propriedades.

<dl> <dt>

**MDHost**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica um host com um agente de email capaz de entregar email para o domínio especificado.

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

[**Método CreateInstanceFromPropertyData da \_ classe MDType MicrosoftDNS**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ MDType**](microsoftdns-mdtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





