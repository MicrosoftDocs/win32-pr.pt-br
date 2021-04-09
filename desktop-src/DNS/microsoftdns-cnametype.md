---
title: Classe MicrosoftDNS_CNAMEType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de nome canônico (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType de classe de DNS
- MicrosoftDNS_CNAMEType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dca8729c2c750e1cef774b5f0f3eadc3e2f6fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824418"
---
# <a name="microsoftdns_cnametype-class"></a>\_Classe cnametype MicrosoftDNS

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de nome canônico (CNAME).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a>Membros

A **classe \_ cnametype MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ cnametype MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um registro de recurso CNAME com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o nome primário do registro CNAME. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o TTL e o nome primário para os valores especificados como os parâmetros de entrada deste método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                        |



 

### <a name="properties"></a>Propriedades

A **classe \_ cnametype MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Primárioname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Canônico ou nome primário para o proprietário do registro CNAME.

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

[**Método CreateInstanceFromPropertyData da \_ classe cnametype MicrosoftDNS**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ cnametype**](microsoftdns-cnametype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





