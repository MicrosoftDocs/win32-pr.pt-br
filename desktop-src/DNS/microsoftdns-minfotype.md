---
title: MicrosoftDNS_MINFOType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro MINFO (Informações de Email).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- dns MicrosoftDNS_MINFOType classe
- MicrosoftDNS_MINFOType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6c04f6d87663534f9d1743ce09990de86fed9f7a16f78f26643f868554f58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967398"
---
# <a name="microsoftdns_minfotype-class"></a>Classe MINFOType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord que**](microsoftdns-resourcerecord.md) representa um registro MINFO (Informações de Email).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a>Membros

A **classe \_ MINFOType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ MINFOType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Insinua um tipo MINFO de RR com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário da lista/caixa de email, a classe (padrão = IN), o valor de vida real e as caixas de correio responsáveis e de erro. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Esse método atualiza o TTL, a Caixa de Correio Responsável e a Caixa de Correio de Erro para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>    |



 

### <a name="properties"></a>Propriedades

A **classe \_ MINFOType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**ErrorMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN especificando uma caixa de correio para receber mensagens de erro relacionadas à lista de correspondência ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.

</dd> <dt>

**ResponsibleMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN especificando uma caixa de correio responsável pela lista de correspondência ou caixa de correio especificada no Nome do Proprietário do registro.

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

[**Método CreateInstanceFromPropertyData da classe MINFOType do MicrosoftDNS \_**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MINFOType do MicrosoftDNS \_**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





