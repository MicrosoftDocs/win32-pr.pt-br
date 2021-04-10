---
description: Indica se o componente de minutos no valor de data e hora CIM contém um intervalo ou um valor curinga.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. MinutesSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091294"
---
# <a name="swbemdatetimeminutesspecified-property"></a>Propriedade SWbemDateTime. MinutesSpecified

A propriedade **MinutesSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de minutos no valor DateTime do CIM contém um intervalo ou um valor curinga. Se **MinutesSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false** (indicando que o valor de DateTime de CIM não tem curingas), então [**SWbemDateTime. Minutes**](swbemdatetime-minutes.md) contém um valor de data. Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** . Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) for **false** e **isinterval** for **true**, **SWbemDateTime. Minutes** conterá um intervalo.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | ISWbemDateTime de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime. minutos**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[HORÁRIO](datetime.md)
</dt> </dl>

 

 




