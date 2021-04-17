---
description: Valor booliano que indica se o componente UTC (horário coordenado universal) no valor de data e hora do CIM contém um intervalo ou um valor curinga.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime. UTCSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790638"
---
# <a name="swbemdatetimeutcspecified-property"></a>Propriedade SWbemDateTime. UTCSpecified

A propriedade **UTCSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliano que indica se o componente UTC (horário coordenado universal) no valor DateTime do CIM contém um intervalo ou um valor curinga. Se **UTCSpecified** for **true** e [**isinterval**](swbemdatetime-isinterval.md) for **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) conterá um valor [**DateTime**](datetime.md) . Um valor **DateTime** que contém um intervalo não pode ser convertido no formato **de \_ Data VT** ou no formato **FILETIME** . Se **UTCSpecified** for **false** e **isinterval** for **true**, **SWbemDateTime. UTC** conterá um intervalo.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de [data e hora CIM, consulte formato de datas e horas](date-and-time-format.md).

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

[**SWbemDateTime. UTC**](swbemdatetime-utc.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[HORÁRIO](datetime.md)
</dt> </dl>

 

 




