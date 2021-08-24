---
description: Essa classe é a classe de tipo de evento para eventos de rotina de driver completo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Classe DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac1329c60f38ebfb4597b85ec251e074babd2c1fde7e58fee2423b6a11be92f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814884"
---
# <a name="drivercompletionroutine-class"></a>Classe DriverCompletionRoutine

Essa classe é a classe de tipo de evento para eventos de rotina de driver completo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Membros

A classe **DriverCompletionRoutine** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DriverCompletionRoutine** tem essas propriedades.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Pacote de solicitação de e/s.

</dd> <dt>

**Rotina**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Endereço da função de driver que está sendo chamada.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Identificador que identifica a solicitação de forma exclusiva. Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




