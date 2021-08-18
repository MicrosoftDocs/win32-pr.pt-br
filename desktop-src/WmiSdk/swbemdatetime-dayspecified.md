---
description: Valor booliana que indica se o componente day no valor DATETIME cim contém um intervalo ou um valor curinga.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime.DaySpecified (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: effa3bcb68351aa754006c143e738443efdb7238129f30847876ad17527ca279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992246"
---
# <a name="swbemdatetimedayspecified-property"></a>Propriedade SWbemDateTime.DaySpecified

A **propriedade DaySpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliana que indica se o componente day no valor [**DATETIME**](datetime.md) cim contém um intervalo ou um valor curinga. Se **DaySpecified** for **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) for **FALSE,** [**SWbemDateTime.Day conterá**](swbemdatetime-day.md) um valor datetime. Um [**valor DATETIME**](datetime.md) que contém um intervalo não pode ser convertido no **formato DATE da VT \_** ou **no formato FILETIME.** Se **DaySpecified** for **FALSE** e **IsInterval** **for TRUE,** **SWbemDateTime.Day** conterá um intervalo.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

Para ver exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores CIM [**DATETIME**](datetime.md) de e para o formato **FILETIME** ou **VT \_ DATE,** consulte [Tarefas WMI:](wmi-tasks--dates-and-times.md)Datas e Horas . Para uma descrição do formato CIM **DATETIME,** consulte [Formato de data e hora.](date-and-time-format.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime.Day**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Datetime**](datetime.md)
</dt> </dl>

 

 




