---
description: Essa classe é a classe de tipo de evento para eventos de thread prontos. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Classe ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827268"
---
# <a name="readythread-class"></a>Classe ReadyThread

Essa classe é a classe de tipo de evento para eventos de thread prontos.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a>Membros

A classe **ReadyThread** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ReadyThread** tem essas propriedades.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

O valor pelo qual a prioridade está sendo ajustada.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

O motivo para o aumento de prioridade.



| Valor                                                                        | Significado                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignore o incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Aplique o incremento, que irá decaimento incrementalmente ao final de cada Quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Aplique o incremento como um aumento que será decaimentodo em sua totalidade no Quantum (normalmente para doação de prioridade).<br/> |



 

</dd> <dt>

Sinalizador
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

A seguir estão os possíveis sinalizadores de Estado:



| Valor                                                                          | Significado                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | O thread foi pronto do DPC (chamada de procedimento adiado).<br/> |
| <dl> <dt>0x2</dt> </dl> | A pilha do kernel está permutada no momento.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | O espaço de endereço do processo é trocado.<br/>                       |



 

Observe que, quando a pilha do kernel ou o espaço de endereço do processo for trocado, haverá um evento ReadyThread adicional depois que a pilha do kernel ou o espaço de endereço do processo tiver sido trocado novamente e o thread estiver pronto para ser despachado.

</dd> <dt>

Reservado
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5)
</dt> </dl>

Reservado.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), formato ("x")
</dt> </dl>

O identificador de thread do thread que está sendo pronto para execução.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Thread \_ v2**](thread-v2.md)
</dt> </dl>

 

 




