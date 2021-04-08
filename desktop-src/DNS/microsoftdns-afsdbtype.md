---
title: Classe MicrosoftDNS_AFSDBType
description: Subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro AFSDB (servidor de banco de dados do sistema de arquivos Andrew).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType de classe de DNS
- MicrosoftDNS_AFSDBType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009384"
---
# <a name="microsoftdns_afsdbtype-class"></a>\_Classe MicrosoftDNS AFSDBType

Subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro AFSDB (servidor de banco de dados do sistema de arquivos Andrew).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ AFSDBType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ AFSDBType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um registro de recurso AFSDB com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/da célula, a classe (padrão = IN), o valor de vida útil e o subtipo e o nome do servidor AFS do host. Retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Esse método atualiza o TTL, o subtipo e o nome do servidor para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>   |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ AFSDBType** tem essas propriedades.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica um host que tem um servidor para a célula AFS especificada no nome do proprietário.

</dd> <dt>

**Subtipo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Subtipo do servidor host AFS. Para o subtipo 1 (valor = 1), o host tem um servidor de local de volume AFS versão 3,0 para a célula AFS nomeada. No caso do subtipo 2 (valor = 2), o host tem um servidor de nomes autenticado que contém o nó do diretório raiz da célula para a célula de DCE/NCA nomeada.

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

[**Método CreateInstanceFromPropertyData da \_ classe AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





