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
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971535"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



 

 




