---
description: Converte um valor de data e hora no formato DATETIME CIM no formato DATE da \_ VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime.GetVarDate (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 506c897da130b9558b37637918674a7c6024adb787ac3d91e53e430a6edfcd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314751"
---
# <a name="swbemdatetimegetvardate-method"></a>Método SWbemDateTime.GetVarDate

O **método GetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte um valor de data e hora no formato [**DATETIME**](datetime.md) CIM para o **formato DATE da VT. \_**

O **formato DATE \_ da VT** é um valor [**DATETIME**](datetime.md) variante de automação que Visual Basic e ActiveX usar.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsLocal* \[ in, opcional\]
</dt> <dd>

Indica se o valor retornado é interpretado como hora local. A Tempo Universal Coordenado (UTC) contém a hora local convertida no deslocamento UTC correto. Se o valor for **FALSE,** o valor será interpretado como UTC com um deslocamento de zero (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de data e hora no **formato DATE da VT. \_**

## <a name="remarks"></a>Comentários

**VT \_ Os valores DATE** **e FILETIME** não podem conter campos curinga.

O **método GetVarDate** falhará (**wbemErrFailed**) se qualquer uma das seguintes propriedades for **FALSE:**

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**Minutos Especificados**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**Microssegundos Especificados**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

No retorno bem-sucedido [**de SetVarDate,**](swbemdatetime-setvardate.md)todas essas propriedades são definidas como **TRUE.**

Após uma chamada bem-sucedida para [**SetVarDate**](swbemdatetime-setvardate.md), o valor [**DATETIME**](datetime.md) sempre é interpretado como um valor **DATETIME** absoluto em vez de um intervalo e [**IsInterval**](swbemdatetime-isinterval.md) é definido como **FALSE.**

Se [**IsInterval**](swbemdatetime-isinterval.md) for definido como **TRUE,** uma chamada para **GetVarDate** resulta no **erro wbemErrFailed.**

Alguma perda de precisão ocorre quando você chama **GetVarDate**, porque os valores [datetime](datetime.md) têm uma resolução de um microssegundo ( s) e os valores **date da VT \_** têm uma resolução de 500 milissegundos.

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

[**SWbemDateTime.GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[Datetime](datetime.md)
</dt> </dl>

 

 




