---
title: Tipos de dados de log de eventos do Windows (WinEvt. h)
description: O log de eventos do Windows define os seguintes tipos de dados
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644621"
---
# <a name="windows-event-log-data-types"></a>Tipos de dados de log de eventos do Windows

O log de eventos do Windows define os seguintes tipos de dados:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_alça EVT**
</dt> <dd>

Um identificador para um objeto de log de eventos do Windows.

</dd> <dt>

**identificador de PEVT \_**
</dt> <dd>

Um ponteiro para o identificador de um objeto de log de eventos do Windows.

</dd> <dt>

**\_identificador da \_ propriedade da matriz de objetos EVT \_ \_**
</dt> <dd>

Um identificador para uma matriz de objetos de log de eventos do Windows.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





