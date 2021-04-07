---
title: Tipos de datanap (NapTypes. h)
description: 'Observação: a plataforma de proteção de acesso à rede não está disponível a partir do Windows 10 os tipos de DataType para a API NAP (proteção de acesso à rede) são os seguintes.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Experiênciatime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Percentual
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918947"
---
# <a name="nap-datatypes"></a>Tipos de datanap

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

Os tipos de texto da API NAP (proteção de acesso à rede) são os seguintes.


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

**Experiênciatime**
</dt> <dd>

Uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém um tempo relacionado à experiência de um computador cliente.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Um valor que especifica o intervalo de valores possíveis para o tamanho máximo, em bytes, de um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) , conforme definido pelo intervalo ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Um identificador exclusivo de 4 bytes usado por SHAs, SHVs e clientes de imposição para se identificar. Os três primeiros bytes são o código de SMI atribuído pela IETF do fornecedor e o último byte identifica o próprio componente.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Um valor de **NapComponentId** usado para identificar pares de Sha/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Um valor de **NapComponentId** usado para identificar clientes de imposição.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Um valor que especifica o número de SHAs registrados no sistema NAP no intervalo de 0 (zero) a [**maxSystemHealthEntityCount**](nap-type-constants.md).

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Um valor que especifica o número de clientes de imposição no sistema NAP no intervalo de 0 (zero) a [**maxEnforcerCount**](nap-type-constants.md).

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

A versão de [**contado**](/windows/win32/api/naptypes/ns-naptypes-countedstring) de uma estrutura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) usada para emparelhar [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) com **SoHResponses**.

</dd> <dt>

**ConnectionId**
</dt> <dd>

Um GUID (identificador global exclusivo) exclusivo usado para identificar conexões NAP mantidas por clientes de imposição.

</dd> <dt>

**Percentual**
</dt> <dd>

Um valor que contém a porcentagem entre 0 (zero) e 100 de correções concluídas

</dd> <dt>

**MessageId**
</dt> <dd>

Um valor exclusivo usado para identificar mensagens do sistema NAP.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>NapTypes. h; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



 

