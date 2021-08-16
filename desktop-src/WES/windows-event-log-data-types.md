---
title: Windows Tipos de dados de log de eventos (WinEvt. h)
description: Windows O log de eventos define os seguintes tipos de dados
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c309dd52471bd501aa2668220d39882ab8de7e1c23a646084364659df4ae4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619986"
---
# <a name="windows-event-log-data-types"></a>Windows Tipos de dados de log de eventos

Windows O log de eventos define os seguintes tipos de dados:


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**\_alça EVT**
</dt> <dd>

um identificador para um objeto de Log de eventos Windows.

</dd> <dt>

**identificador de PEVT \_**
</dt> <dd>

um ponteiro para o identificador de um objeto de Log de eventos Windows.

</dd> <dt>

**\_identificador da \_ propriedade da matriz de objetos EVT \_ \_**
</dt> <dd>

um identificador para uma matriz de Windows objetos de Log de eventos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>WinEvt. h</dt> </dl> |



 

 





