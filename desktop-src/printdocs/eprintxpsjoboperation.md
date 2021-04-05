---
description: Especifica se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumeração EPrintXPSJobOperation (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662119"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Enumeração EPrintXPSJobOperation

Especifica se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

O trabalho XPS está em spool.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

O trabalho XPS está sendo renderizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada principalmente como um parâmetro para a função [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



 

 




