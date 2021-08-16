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
ms.openlocfilehash: 1b4b3d63b63e4deb9c48f9e117122f021e9d63791292e60da3cc919a6e4535e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069806"
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

A **classe ReadyThread** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe ReadyThread** tem essas propriedades.

<dl> <dt>

AdjustIncrement
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

O valor pelo qual a prioridade está sendo ajustada.

</dd> <dt>

AdjustReason
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

O motivo do aumento de prioridade.



| Valor                                                                        | Significado                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ignore o incremento.<br/>                                                                                        |
| <dl> <dt>1</dt> </dl> | Aplique o incremento, que será decair incrementalmente no final de cada quantum.<br/>                              |
| <dl> <dt>2</dt> </dl> | Aplique o incremento como um aumento que decairá em sua totalidade em quantum (normalmente para a prioridade de prioridade).<br/> |



 

</dd> <dt>

Sinalizador
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

Veja a seguir os possíveis sinalizadores de estado:



| Valor                                                                          | Significado                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0x1</dt> </dl> | O thread foi lido do DPC (chamada de procedimento adiado).<br/> |
| <dl> <dt>0x2</dt> </dl> | No momento, a pilha de kernel é trocada.<br/>                      |
| <dl> <dt>0x4</dt> </dl> | O espaço de endereço do processo é trocado.<br/>                       |



 

Observe que quando a pilha do kernel ou o espaço de endereço do processo for trocado, haverá um evento ReadyThread adicional após a pilha do kernel ou o espaço de endereço do processo ter sido trocado novamente e o thread estiver pronto para ser expedido.

</dd> <dt>

Reservado
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(5)
</dt> </dl>

Reservado.

</dd> <dt>

TThreadId
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1), Format("x")
</dt> </dl>

O identificador de thread do thread que está sendo lido para execução.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Thread \_ V2**](thread-v2.md)
</dt> </dl>

 

 




