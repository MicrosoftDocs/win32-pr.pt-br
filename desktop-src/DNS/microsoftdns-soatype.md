---
title: MicrosoftDNS_SOAType classe
description: A subclasse do MicrosoftDNS \_ ResourceRecord que representa um registro SOA (Start Of Authority).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- dns MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType classe DNS , descrita
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
ms.openlocfilehash: ad2a9b0317c6e842558f771dcd10ec7707602e17510ffc20c3a9684fc94bf7d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163140"
---
# <a name="microsoftdns_soatype-class"></a>Classe SOAType do MicrosoftDNS \_

A subclasse [**do MicrosoftDNS \_ ResourceRecord que**](microsoftdns-resourcerecord.md) representa um registro SOA (Start Of Authority).

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

A **classe \_ SOAType do MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ SOAType do MicrosoftDNS** tem esses métodos.



| Método     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modificar** | Atualiza o TTL, o Número de Série SOA, o Servidor Primário, a Parte Responsável, o Intervalo de Atualização, o Atraso de Nova Tentativa, o Limite de Expiração e o TTL Mínimo (para a zona) para os valores especificados como os parâmetros de entrada desse método. Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado. O método retorna uma referência ao objeto modificado como um parâmetro de saída. <br/> Qualificadores: implementados<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ SOAType do MicrosoftDNS** tem essas propriedades.

<dl> <dt>

**ExpireLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes que uma zona sem resposta não seja mais autoritativa.

</dd> <dt>

**MinimumTTL**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Limite inferior no tempo, em segundos, em que um servidor DNS ou um resolvedor Caching tem permissão para armazenar em cache qualquer registro de recurso da zona à qual esse registro pertence.

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

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes que a zona que contém esse registro seja atualizada.

</dd> <dt>

**ResponsibleParty**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome da parte responsável pela zona à qual o registro pertence.

</dd> <dt>

**RetryDelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tempo, em segundos, antes de tentar novamente uma atualização com falha da zona à qual esse registro pertence.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
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
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método Modify da classe SOAType do MicrosoftDNS \_**](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





