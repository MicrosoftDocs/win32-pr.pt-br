---
description: Indica se o componente minutes no valor datetime cim contém um intervalo ou um valor curinga.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Propriedade SWbemDateTime.MinutesSpecified (Wbemdisp.h)
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
ms.openlocfilehash: a780d9bed3224e1b9be006a2bdf94b2b411951ceb3ef4d82a439ba5ec451fd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992186"
---
# <a name="swbemdatetimeminutesspecified-property"></a>Propriedade SWbemDateTime.MinutesSpecified

A **propriedade MinutesSpecified** do objeto [**SWbemDateTime**](swbemdatetime.md) é um valor booliana que indica se o componente minutes no valor datetime cim contém um intervalo ou um valor curinga. Se **MinutesSpecified** for **TRUE** e [**IsInterval**](swbemdatetime-isinterval.md) for **FALSE** (indicando que o valor datetime cim não tem curingas), [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) conterá um valor de data. Um valor datetime que contém um intervalo não pode ser convertido no **formato DATE da VT \_** ou **no formato FILETIME.** Se [**HoursSpecified**](swbemdatetime-hoursspecified.md) for **FALSE** e **IsInterval** **for TRUE,** **SWbemDateTime.Minutes** conterá um intervalo.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemDateTime.MinutesSpecified As boolean
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

[**SWbemDateTime.Minutes**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




