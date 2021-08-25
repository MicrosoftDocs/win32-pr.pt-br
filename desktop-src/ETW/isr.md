---
description: Essa classe é a classe de tipo de evento para eventos de ISR (rotina de serviço de interrupção). A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: Classe ISR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 621bf9c97aef9ea23fba6186a419f7c205d98fba608c2539702607986de0d258
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900996"
---
# <a name="isr-class"></a>Classe ISR

Essa classe é a classe de tipo de evento para eventos de ISR (rotina de serviço de interrupção).

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>Membros

A classe **ISR** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ISR** tem essas propriedades.

<dl> <dt>

**Inicialtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), extensão ("WmiTime")
</dt> </dl>

Tempo de entrada de ISR.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), ponteiro
</dt> </dl>

Reservado.

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Booliano que indica se a interrupção foi reivindicada (é true se a interrupção foi reivindicada).

</dd> <dt>

**Rotina**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Endereço da rotina de ISR. Use o endereço com os eventos de imagem para descobrir qual imagem foi iniciada.

</dd> <dt>

**Vetor**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Vetor da tabela de descritor de interrupção à qual a rotina de ISR é atribuída.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




