---
title: MicrosoftDNS_NXTType classe
description: Subclasse do MicrosoftDNS \_ ResourceRecord que representa um RR next (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- dns MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType classe DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36fa67d3d1ab60aa4af6c0be7269f068edaf42a64fa9cf1cfea68ca23d82ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913096"
---
# <a name="microsoftdns_nxttype-class"></a>Classe \_ NXTType do MicrosoftDNS

Subclasse [**do MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um RR next (NXT).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a>Membros

A **classe \_ NXTType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ NXTType do MicrosoftDNS** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Institui um Registro de Recurso NXT com base nos dados nos parâmetros de entrada do método: o Nome do Servidor DNS do registro, o Nome do Contêiner, o Nome do Proprietário, a classe (padrão = IN), o valor de vida real e o sinalizador de mapeamento WINS, o tempo de pesquisa reverso, o tempo de tempo de cache wins e o nome de domínio a ser anexado. Ele retorna uma referência ao novo objeto como um parâmetro de saída. <br/> Qualificadores: implementados, estáticos<br/>                                                                                                                                           |
| **Modificar**                         | Atualiza o TTL, o Sinalizador de Mapeamento, o Tempo De Busca, o Tempo De Saída do Cache e o Domínio de Resultado para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> **Windows Server 2003:** Esse método também atualiza NextDomainName e Types para os valores especificados como os parâmetros de entrada desse método.<br/> <br/> |



 

### <a name="properties"></a>Propriedades

A **classe MicrosoftDNS \_ NXTType** tem essas propriedades.

<dl> <dt>

**NextDomainName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Próximo nome de domínio.

</dd> <dt>

**Types**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista separada por espaço dos mnemônicos do tipo RR para o nome do proprietário do Registro de Recurso NXT.

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

[**Método CreateInstanceFromPropertyData da classe NXTType do MicrosoftDNS \_**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify da classe \_ NXTType do MicrosoftDNS**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





