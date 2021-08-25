---
title: MicrosoftDNS_WKSType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro WKS (Well-Known Services).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- dns MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a6621e3dedacd5520c00b71c66bf0091c31135b70f27486ba43da63f393da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874756"
---
# <a name="microsoftdns_wkstype-class"></a>Classe WKSType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro WKS (Well-Known Services).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a>Membros

A **classe \_ WKSType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ WKSType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Insere um tipo WKS de RR com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida real e o Endereço da Internet, o protocolo IP e a máscara de bit de porta do proprietário. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/>  |
| **Modificar**                         | Esse método atualiza o TTL, o Endereço da Internet, o Protocolo IP e os Serviços para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ WKSType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**InternetAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Endereço IP da Internet para o proprietário do registro.

</dd> <dt>

**IPProtocol**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres que representa o protocolo IP para esse registro. Os valores válidos são UDP ou TCP.

</dd> <dt>

**Serviços**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres que contém todos os serviços usados pelo registro WKS (Well Known Service).

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

[**Método CreateInstanceFromPropertyData da classe WKSType do MicrosoftDNS \_**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe WKSType do MicrosoftDNS \_**](microsoftdns-wkstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





