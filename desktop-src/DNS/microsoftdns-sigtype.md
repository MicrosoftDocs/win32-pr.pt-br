---
title: MicrosoftDNS_SIGType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um Registro de Recurso de Assinatura (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- dns MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType classe DNS, descrita
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
ms.openlocfilehash: e17009bf6458bd51b1d7a41b31f33ad0695e0da1a41c77aa72f56ee01573a529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163167"
---
# <a name="microsoftdns_sigtype-class"></a>Classe SIGType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord que**](microsoftdns-resourcerecord.md) representa um Registro de Recurso de Assinatura (SIG).

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

A **classe \_ SIGType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ SIGType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Institui um RR SIG com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida real e o sinalizador de mapeamento WINS, o tempo de pesquisa inversa, o tempo de tempo de recuperação reverso, o tempo de cache WINS e o nome de domínio a ser anexado. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/>                                                                                                                                                                                                                                                       |
| **Modificar**                         | Atualiza o TTL, o Sinalizador de Mapeamento, o Tempo De Busca, o Tempo De Saída do Cache e o Domínio de Resultado para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> **Windows Server 2003:** Esse método também atualiza TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName e Signature para os valores especificados como os parâmetros de entrada desse método.<br/> <br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ SIGType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**Algoritmo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Algoritmo usado com a chave especificada no registro de recurso. Os valores atribuídos são mostrados na tabela a seguir.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografia de curva elíptica<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Método usado para escolher uma chave que verifica uma SIG. Consulte RFC 2535, Apêndice C para o método usado para calcular uma KeyTag.

</dd> <dt>

**Rótulos**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contagem sem sinal de rótulos no nome do proprietário original do SIG RR. A contagem não inclui o rótulo NULL para a raiz, nem nenhum curinga inicial.

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

TTL do conjunto de RR assinado pela SIG.

</dd> <dt>

**Assinatura**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Assinatura, representada na base 64, formatada conforme definido no RFC 2535, Apêndice A.

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, Horário de Greenwich (GMT), excluindo segundos bissexto.

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora em que a Assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, GMT (Hora Média de Greenwich), excluindo os segundos bissexto.

</dd> <dt>

**SignerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de domínio do signante que gerou o SIG RR.

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
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
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método CreateInstanceFromPropertyData da classe SIGType do MicrosoftDNS \_**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe SIGType do MicrosoftDNS \_**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





