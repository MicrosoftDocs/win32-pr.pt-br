---
title: Classe MicrosoftDNS_MINFOType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro MINFO (mail information).
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType de classe de DNS
- MicrosoftDNS_MINFOType de classe de DNS, descrita
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
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086308"
---
# <a name="microsoftdns_minfotype-class"></a>\_Classe MicrosoftDNS MINFOType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro MINFO (mail information).

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

A classe **MicrosoftDNS \_ MINFOType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ MINFOType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um tipo MINFO de RR com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário da lista/caixa de email, a classe (padrão = IN), o valor de vida útil e as caixas de correio de erro e responsável. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Esse método atualiza a TTL, a caixa de correio responsável e a caixa de correio de erro para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>    |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ MINFOType** tem essas propriedades.

<dl> <dt>

**ErrorMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica uma caixa de correio para receber mensagens de erro relacionadas à lista de endereçamento ou à caixa de correio especificada pelo nome do proprietário do registro MINFO.

</dd> <dt>

**ResponsibleMailbox**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

FQDN que especifica uma caixa de correio responsável pela lista de endereçamento ou caixa de correio especificada no nome do proprietário do registro.

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

[**Método CreateInstanceFromPropertyData da \_ classe MINFOType MicrosoftDNS**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





