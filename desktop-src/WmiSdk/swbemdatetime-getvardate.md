---
description: Converte um valor de data e hora no formato CIM DATETIME no formato de \_ Data VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetVarDate (Wbemdisp. h)
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
# <a name="swbemdatetimegetvardate-method"></a>Método SWbemDateTime. GetVarDate

O método **GetVarDate** do objeto [**SWbemDateTime**](swbemdatetime.md) converte um valor de data e hora no formato CIM [**DateTime**](datetime.md) no formato de **\_ Data VT** .

o formato de **\_ data VT** é um valor [**DATETIME**](datetime.md) de variante de automação que Visual Basic e ActiveX uso.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsLocal* \[ em, opcional\]
</dt> <dd>

Indica se o valor retornado é interpretado como hora local. A propriedade UTC (tempo Universal Coordenado) contém a hora local convertida para o deslocamento UTC correto. Se o valor for **false**, o valor será interpretado como UTC com um deslocamento zero (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de data e hora no formato de **\_ Data VT** .

## <a name="remarks"></a>Comentários

**VT \_** Os valores de data e **FILETIME** não podem conter campos curinga.

O método **GetVarDate** falhará (**wbemErrFailed**) se qualquer uma das seguintes propriedades for **falsa**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

Após o retorno bem-sucedido de [**SetVarDate**](swbemdatetime-setvardate.md), todas essas propriedades são definidas como **true**.

Após uma chamada bem-sucedida para [**SetVarDate**](swbemdatetime-setvardate.md), o valor [**DateTime**](datetime.md) é sempre interpretado como um valor **DateTime** absoluto, em vez de um intervalo, e o [**isinterval**](swbemdatetime-isinterval.md) é definido como **false**.

Se [**isinterval**](swbemdatetime-isinterval.md) for definido como **true**, uma chamada para **GetVarDate** resultará no erro **wbemErrFailed** .

Uma perda de precisão ocorre quando você chama **GetVarDate**, pois os valores de [DateTime](datetime.md) têm uma resolução de um microssegundo (s) e os valores de **\_ data VT** têm uma resolução de 500 milissegundos.

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM para e do formato de **\_ dados** **FILETIME** ou VT, consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | ISWbemDateTime de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemDateTime. GetFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[HORÁRIO](datetime.md)
</dt> </dl>

 

 




