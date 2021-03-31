---
title: Classe MicrosoftDNS_SIGType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de recurso de assinatura (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType de classe de DNS
- MicrosoftDNS_SIGType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644340"
---
# <a name="microsoftdns_sigtype-class"></a>\_Classe MicrosoftDNS SIGType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de recurso de assinatura (SIG).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ SIGType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ SIGType** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cria uma instância de um RR SIG com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa inversa, o tempo limite do cache WINS e o nome de domínio a acrescentar. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/>                                                                                                                                                                                                                                                       |
| **Modificar**                         | Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e o domínio de resultado para os valores especificados como os parâmetros de entrada deste método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> **Windows Server 2003:** Esse método também atualiza TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, Signatárioname e assinatura para os valores especificados como os parâmetros de entrada desse método.<br/> <br/> |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ SIGType** tem essas propriedades.

<dl> <dt>

**Algoritmo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Algoritmo usado com a chave especificada no registro de recurso. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Método usado para escolher uma chave que verifica um SIG. Consulte RFC 2535, Apêndice C para o método usado para calcular um KeyTag.

</dd> <dt>

**Rótulos**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contagem não assinada de rótulos no nome do proprietário do RR SIG original. A contagem não inclui o rótulo nulo para a raiz nem qualquer caractere curinga inicial.

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

TTL do conjunto de RRs assinado pelo SIG.

</dd> <dt>

**Signature**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Assinatura, representada na base 64, formatada conforme definido na RFC 2535, apêndice A.

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, hora de Greenwich (GMT), excluindo segundos bissextos.

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que a assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, Greenwich Mean Time (GMT), excluindo segundos bissextos.

</dd> <dt>

**Signatárioname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de domínio do signatário que gerou o RR SIG.

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de RR coberto por essa SIG.

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

[**Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ SIGType**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





