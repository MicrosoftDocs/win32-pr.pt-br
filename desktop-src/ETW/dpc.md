---
description: Essa classe é a classe de tipo de evento para eventos DPC (chamada de procedimento deferida) do dispositivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Classe DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826874"
---
# <a name="dpc-class"></a>Classe DPC

Essa classe é a classe de tipo de evento para eventos DPC (chamada de procedimento deferida) do dispositivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>Membros

A classe **DPC** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DPC** tem essas propriedades.

<dl> <dt>

**Inicialtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), extensão ("WmiTime")
</dt> </dl>

Tempo de entrada de DPC.

</dd> <dt>

**Rotina**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Endereço da rotina de DPC. Use o endereço com os eventos de imagem para descobrir qual imagem foi iniciada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses eventos são registrados quando um DPC é inserido. Você usa esses eventos para monitorar e verificar o comportamento de drivers e componentes do modo kernel. Por exemplo, você pode usar eventos DPC, ISR e Image para determinar os componentes que gastam muito tempo em níveis altos de interrupção. Os eventos DPC e ISR têm um carimbo de data/hora de entrada que é usado para calcular a duração das rotinas. Os eventos de imagem são lidos para construir as regiões de memória que são mapeadas para determinados módulos. Você pode usar o mapeamento para localizar o módulo que contém a rotina de interrupção.

O evento TimerDPC registra quando um DPC é acionado como resultado de uma expiração do temporizador e dos registros de evento ThreadDPC quando um DPC thread é executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




