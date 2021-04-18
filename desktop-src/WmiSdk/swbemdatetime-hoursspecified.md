---
description: A propriedade HoursSpecified do objeto SWbemDateTime é um valor booliano que indica se o componente de horas no valor DateTime do CIM contém um intervalo ou um valor curinga.
ms.assetid: 55211da6-cbd5-4e61-ab7d-ee20363e9d81
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. HoursSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.HoursSpecified
- ISWbemDateTime.HoursSpecified
- ISWbemDateTime.get_HoursSpecified
- ISWbemDateTime.put_HoursSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e092747768035b7948ddef66f4c4d542bfa2c38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781455"
---
# <a name="swbemdatetimehoursspecified-property"></a>Propriedade SWbemDateTime. HoursSpecified

A propriedade **HoursSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente de horas no valor DateTime do CIM contém um intervalo ou um valor curinga. Se **HoursSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. Hours**](swbemdatetime-hours.md) conterá um valor DateTime. Um valor DateTime que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** . Se **HoursSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. Hours** conterá um intervalo.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.HoursSpecified As Boolean
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

[**SWbemDateTime. horas**](swbemdatetime-hours.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[HORÁRIO](datetime.md)
</dt> </dl>

 

 




