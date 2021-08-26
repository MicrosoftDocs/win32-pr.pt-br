---
title: MicrosoftDNS_ISDNType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- dns MicrosoftDNS_ISDNType classe
- MicrosoftDNS_ISDNType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af06ad782b6d36213e9a1df210916f9346e1e4f8bd0a98dd619651a579dc5c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131716"
---
# <a name="microsoftdns_isdntype-class"></a>Classe ISDNType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro ISDN.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a>Membros

A **classe \_ ISDNType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ ISDNType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instalita um Registro de Recurso ISDN com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida real e o número ISDN e o endereço subddress do proprietário. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o TTL, o Número ISDN e o Subddress para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                   |



 

### <a name="properties"></a>Propriedades

A **classe \_ ISDNType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**ISDNNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número ISDN e DDI do proprietário do registro.

</dd> <dt>

**Subendereço**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Subddress do proprietário, se definido.

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

[**Método CreateInstanceFromPropertyData da classe ISDNType do MicrosoftDNS \_**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe \_ ISDNType do MicrosoftDNS**](microsoftdns-isdntype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





