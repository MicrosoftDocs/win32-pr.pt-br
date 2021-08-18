---
title: MicrosoftDNS_PTRType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro PTR (Ponteiro).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- dns MicrosoftDNS_PTRType classe
- MicrosoftDNS_PTRType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c78cf945ff58071930e5e65fec08f075ddb9337977e6cd5575853e9c437a73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076750"
---
# <a name="microsoftdns_ptrtype-class"></a>Classe PTRType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord que**](microsoftdns-resourcerecord.md) representa um registro PTR (Ponteiro).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a>Membros

A **classe \_ PTRType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ PTRType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instania um Registro de Recurso PTR DNS com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida e o FQDN do registro PTR. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o nome de domínio TTL e PTR para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                 |



 

### <a name="properties"></a>Propriedades

A **classe \_ PTRType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**PTRDomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN dos dados de registro PTR.

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

[**Método CreateInstanceFromPropertyData da classe PTRType do MicrosoftDNS \_**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe PTRType MicrosoftDNS \_**](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





