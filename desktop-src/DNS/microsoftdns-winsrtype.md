---
title: MicrosoftDNS_WINSRType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro WINSR (Reverse Look up).
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- dns MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89c9545c73a4dbd5a01ff401c7b5587cf448553fcafcf4d698e3aeb17ed8722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912816"
---
# <a name="microsoftdns_winsrtype-class"></a>Classe WINSRType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord que**](microsoftdns-resourcerecord.md) representa um registro WINSR (Reverse Look up).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a>Membros

A **classe \_ WINSRType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ WINSRType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Institui um tipo WINSR de RR com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida real e o sinalizador de mapeamento WINS, o tempo de pesquisa reverso, o tempo de tempo de cache wins e o nome de domínio a ser anexado. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/> |
| **Modificar**                         | Atualiza o TTL, o Sinalizador de Mapeamento, o Tempo De Busca, o Tempo De Saída do Cache e o Domínio de Resultado para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/>                        |



 

### <a name="properties"></a>Propriedades

A **classe \_ WINSRType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, em que um servidor DNS usando a Consulta WINS pode armazenar em cache a resposta do servidor WINS.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo acima, em segundos, para um servidor DNS usando a Busca Inversa do WINS.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Sinalizador de mapeamento WINSR que especifica se o registro deve ser incluído na replicação de zona. Ele pode ter apenas dois valores: 0x80000000 e 0x00010000 correspondentes aos sinalizadores de replicação e sem replicação (registro local), respectivamente.

</dd> <dt>

**ResultDomain**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de domínio a ser anexado aos nomes NetBIOS retornados.

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

[**Método CreateInstanceFromPropertyData da classe WINSRType do MicrosoftDNS \_**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe WINSRType do MicrosoftDNS \_**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





