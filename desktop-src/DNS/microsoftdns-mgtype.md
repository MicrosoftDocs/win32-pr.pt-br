---
title: Classe MicrosoftDNS_MGType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de grupo de emails (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType de classe de DNS
- MicrosoftDNS_MGType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4a9b1f88a3d7e2752d2e4c199c261b49364ab7bdcbf4543e852f5218111491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692596"
---
# <a name="microsoftdns_mgtype-class"></a>\_Classe MicrosoftDNS MGType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de grupo de emails (mg).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ MGType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ MGType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Esse método instancia um tipo MG de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário do grupo de emails, a classe (padrão = IN), o valor de vida útil e o nome da caixa de correio. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Esse método atualiza a caixa de correio TTL e MG para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ MGType** tem essas propriedades.

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica uma caixa de correio que é membro do grupo de emails especificado pelo nome do proprietário do registro.

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

[**Método CreateInstanceFromPropertyData da \_ classe MGType MicrosoftDNS**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ MGType**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





