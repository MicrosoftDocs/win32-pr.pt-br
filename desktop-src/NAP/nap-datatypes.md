---
title: Nap Datatypes (NapTypes.h)
description: Observação A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10 Os tipos de dados para a API NAP (Proteção de Acesso à Rede) são os exemplos a seguir.
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Tempo de Inatividade
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Porcentagem
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550baa14779ccefaec14605938edb6076e7cc332aa9d1a2390ab430f7568e844
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802616"
---
# <a name="nap-datatypes"></a>Tipos de dados NAP

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

Os tipos de dados para a API NAP (Proteção de Acesso à Rede) são os a seguir.


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**Tempo de Inatividade**
</dt> <dd>

Uma [estrutura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém um tempo relacionado à inatividade de um computador cliente.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Um valor que especifica o intervalo de valores possíveis para o tamanho máximo, em bytes, de um pacote [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) conforme definido por range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Um identificador exclusivo de 4 byte usado por SHAs, SHVs e clientes de imposição para se identificar. Os três primeiros bytes são o código SMI atribuído a IETF do fornecedor e o último byte identifica o componente em si.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Um **valor NapComponentId** usado para identificar pares SHA/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Um **valor NapComponentId** usado para identificar os clientes de imposição.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Um valor que especifica o número de SHAs registrados no sistema NAP no intervalo 0 (zero) para [**maxSystemHealthEntityCount.**](nap-type-constants.md)

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Um valor que especifica o número de clientes de imposição no sistema NAP no intervalo 0 (zero) para [**maxEnforcerCount.**](nap-type-constants.md)

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

A [**versão CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de uma [**estrutura CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usada para emparelhar [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) com **SoHResponses.**

</dd> <dt>

**ConnectionId**
</dt> <dd>

Um GUID (Identificador Global Exclusivo) exclusivo usado para identificar conexões NAP mantidas pelos clientes de imposição.

</dd> <dt>

**Percentual**
</dt> <dd>

Um valor que contém o percentual entre 0 (zero) e 100 de correção concluída

</dd> <dt>

**MessageId**
</dt> <dd>

Um valor exclusivo usado para identificar mensagens do sistema NAP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



 

