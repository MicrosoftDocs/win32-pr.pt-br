---
title: Classe MicrosoftDNS_SOAType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de início de autoridade (SOA).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType de classe de DNS
- MicrosoftDNS_SOAType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3e7cb617514e2ed7c8692a866cc80dfc639391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008986"
---
# <a name="microsoftdns_soatype-class"></a>\_Classe MicrosoftDNS SOAType

A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de início de autoridade (SOA).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a>Membros

A classe **MicrosoftDNS \_ SOAType** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MicrosoftDNS \_ SOAType** tem esses métodos.



| Método     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modificar** | Atualiza o TTL, o número de série da SOA, o servidor primário, a parte responsável, o intervalo de atualização, o atraso de repetição, o limite de expiração e o TTL mínimo (para a zona) para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> |



 

### <a name="properties"></a>Propriedades

A classe **MicrosoftDNS \_ SOAType** tem essas propriedades.

<dl> <dt>

**ExpireLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes que uma zona sem resposta não seja mais autoritativa.

</dd> <dt>

**MinimumTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Limite inferior no tempo, em segundos, que um servidor DNS ou um resolvedor de cache tem permissão para armazenar em cache qualquer registro de recurso da zona à qual esse registro pertence.

</dd> <dt>

**PrimaryServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Servidor DNS autoritativo para a zona à qual o registro pertence.

</dd> <dt>

**Intervalo de atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes que a zona que contém esse registro deve ser atualizada.

</dd> <dt>

**ResponsibleParty**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da parte responsável da zona à qual o registro pertence.

</dd> <dt>

**RetryDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes de tentar novamente uma atualização com falha da zona à qual esse registro pertence.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de série do registro SOA.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método Modify da classe MicrosoftDNS \_ SOAType**](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





