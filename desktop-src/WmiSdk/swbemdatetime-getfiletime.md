---
description: Converte um valor de data e hora no formato de datahora CIM no formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739433"
---
# <a name="swbemdatetimegetfiletime-method"></a>Método SWbemDateTime. GetFileTime

O método **GetFileTime** do objeto [**SWbemDateTime**](swbemdatetime.md) converte um valor de data e hora no formato de [DateTime](datetime.md) do CIM para o formato FILETIME.

Se o parâmetro for definido como **true**, o valor de retorno representará uma hora local para o cliente. Caso contrário, o valor de retorno será uma hora UTC (tempo Universal Coordenado). Uma estrutura de [data e hora](datetime.md) **FILETIME** é um valor de 64 bits que representa o número de unidades de 100 nanossegundos desde o início de 1º de janeiro de 1601. Windows A instrumentação de gerenciamento (WMI) trata os valores de **FILETIME** como representações de cadeia de caracteres de números de 64 bits sem sinal.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsLocaL* \[ em, opcional\]
</dt> <dd>

Indica se o valor retornado é interpretado como hora local. A propriedade UTC então contém a hora local convertida no deslocamento UTC (tempo Universal Coordenado) correto. Se o valor for **false**, o valor será interpretado como UTC com um deslocamento zero (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A data e a hora no formato **FILETIME** .

## <a name="error-codes"></a>Códigos do Erro

Depois de concluir o método **GetFileTime** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Falha na chamada.

</dd> </dl>

## <a name="remarks"></a>Comentários

**VT \_** Os valores de data e **FILETIME** não podem conter campos curinga.

O método **filefiletime** falhará (wbemErrFailed) se qualquer uma das seguintes propriedades for **false**:

-   [**YearSpecified**](swbemdatetime-yearspecified.md)
-   [**MonthSpecified**](swbemdatetime-monthspecified.md)
-   [**DaySpecified**](swbemdatetime-dayspecified.md)
-   [**HoursSpecified**](swbemdatetime-hoursspecified.md)
-   [**MinutesSpecified**](swbemdatetime-minutesspecified.md)
-   [**SecondsSpecified**](swbemdatetime-secondsspecified.md)
-   [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)
-   [**UTCSpecified**](swbemdatetime-utcspecified.md)

Em um retorno bem-sucedido de [**SetFileTime**](swbemdatetime-setfiletime.md), todas essas propriedades são definidas como **true**.

## <a name="examples"></a>Exemplos

Para obter exemplos de como usar o objeto [**SWbemDateTime**](swbemdatetime.md) para converter valores de data e [**hora**](datetime.md) CIM de e para o formato **FILETIME** ou o formato de **\_ dados VT** , consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md). Para obter uma descrição do formato de data e hora **CIM,** consulte [formato de datas e horas](date-and-time-format.md).

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

[**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**HORÁRIO**](datetime.md)
</dt> </dl>

 

