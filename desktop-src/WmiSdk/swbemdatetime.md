---
description: O objeto SWbemDateTime é um objeto auxiliar para analisar e definir os valores de data e hora de modelo CIM (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objeto SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790637"
---
# <a name="swbemdatetime-object"></a>Objeto SWbemDateTime

O objeto **SWbemDateTime** é um objeto auxiliar para analisar e definir os valores de [data e hora](datetime.md) de modelo CIM (CIM). Ele desempenha uma função semelhante a [**SWbemObjectPath**](swbemobjectpath.md), que fornece assistência para formatar e interpretar caminhos de objeto. Você pode usar a chamada do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) para criar o objeto **SWbemDateTime** .

Um objeto **SWbemDateTime** pode ser inicializado e formatado em um **VT \_ Date** ou em valores **FILETIME** usando métodos no objeto. Usando as propriedades do objeto, o valor pode ser analisado no ano do componente, mês, dia, hora, minutos, segundos ou em microssegundos. O objeto **SWbemDateTime** pode ser formatado em valores de UTC (tempo Universal local ou coordenado). Para obter mais informações, consulte [formato de data e hora](date-and-time-format.md).

**SWbemDateTime** é o único objeto de script Instrumentação de gerenciamento do Windows (WMI) que é marcado como seguro para inicialização e scripts em execução em páginas HTML no Internet Explorer.

## <a name="members"></a>Membros

O objeto **SWbemDateTime** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemDateTime** tem esses métodos.



| Método                                           | Descrição                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | Converte uma data e hora **FILETIME** , expressa como um **BSTR**, em um formato de [data e hora](datetime.md) WMI.<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | Converte um valor de data e hora formatado de [DateTime](datetime.md) do WMI em uma **\_ Data VT**.<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Converte um formato de [datahora](datetime.md) WMI em uma data e hora **FILETIME** , expressa como um **BSTR**.<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Converte uma data e hora formatadas em **\_ Data VT** em um [DateTime](datetime.md)WMI.<br/>                        |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemDateTime** tem essas propriedades.



| Propriedade                                                                        | Tipo de acesso           | Descrição                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Dia**](swbemdatetime-day.md)<br/>                                     | Leitura/gravação<br/> | O componente de dia de um valor de [data e hora](datetime.md) CIM.<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | Leitura/gravação<br/> | Indica se o dia é especificado ou deixado como um caractere curinga.<br/>                                                        |
| [**Hours**](swbemdatetime-hours.md)<br/>                                 | Leitura/gravação<br/> | As horas do componente de dia de um valor de [data e hora](datetime.md) CIM.<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | Leitura/gravação<br/> | Indica se a hora é especificada ou deixada como um caractere curinga.<br/>                                                       |
| [**Isinterval**](swbemdatetime-isinterval.md)<br/>                       | Leitura/gravação<br/> | Indica que pelo menos um componente do data e [hora](datetime.md) CIM representa um intervalo em vez de uma data.<br/> |
| [**Microssegundos**](swbemdatetime-microseconds.md)<br/>                   | Leitura/gravação<br/> | O componente de microssegundos de um valor de [data e hora](datetime.md) CIM.<br/>                                                  |
| [**MicrosecondsSpecified**](swbemdatetime-microsecondsspecified.md)<br/> | Leitura/gravação<br/> | Indica se o componente de microssegundos é especificado ou deixado como um caractere curinga.<br/>                                     |
| [**minutos**](swbemdatetime-minutes.md)<br/>                             | Leitura/gravação<br/> | O componente de minutos de um valor de [data e hora](datetime.md) CIM.<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | Leitura/gravação<br/> | Indica se o componente de minutos é especificado ou deixado como um caractere curinga.<br/>                                          |
| [**Mês**](swbemdatetime-month.md)<br/>                                 | Leitura/gravação<br/> | O componente de mês de um valor de [data e hora](datetime.md) CIM.<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | Leitura/gravação<br/> | Indica se o mês é especificado ou deixado como um caractere curinga.<br/>                                                      |
| [**Segundos**](swbemdatetime-seconds.md)<br/>                             | Leitura/gravação<br/> | O componente de segundos de um valor de [data e hora](datetime.md) CIM.<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | Leitura/gravação<br/> | Indica se o componente de segundos é especificado ou deixado como um caractere curinga.<br/>                                          |
| [**HORÁRIO**](swbemdatetime-utc.md)<br/>                                     | Leitura/gravação<br/> | O componente UTC de um valor [DateTime](datetime.md) de CIM.<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | Leitura/gravação<br/> | Indica se o componente UTC é especificado ou deixado como um caractere curinga.<br/>                                              |
| [**Valor**](swbemdatetime-value.md)<br/>                                 | Leitura/gravação<br/> | O valor [DateTime](datetime.md) de CIM completo.<br/>                                                                         |
| [**Year**](swbemdatetime-year.md)<br/>                                   | Leitura/gravação<br/> | O componente de ano de um valor de [data e hora](datetime.md) CIM.<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | Leitura/gravação<br/> | Indica se o ano é ou não especificado ou deixado como um caractere curinga.<br/>                                                |



 

## <a name="remarks"></a>Comentários

O WMI registra carimbos de data/hora no formato UTC (Universal Time Coordinate). O UTC não é o formato que a maioria dos desenvolvedores e administradores de ti usam. Portanto, um problema comum é determinar como converter o UTC em algo mais legível. Para obter mais informações sobre como trabalhar com o UTC, consulte [tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md) e [trabalho com datas e horas usando o WMI](/previous-versions/tn-archive/ee198928(v=technet.10)). Você também pode ler os [s de tempo (Ah, e sobre datas também)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) e [como posso subtrair um número especificado de dias de um valor UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) Postagens de blog para obter informações adicionais.

Qualquer campo numérico pode ter um valor curinga se a propriedade [**isinterval**](swbemdatetime-isinterval.md) for definida como **false**. Os campos com valores curinga contêm asteriscos em todo o campo.

Cada propriedade, por exemplo, [**Day**](swbemdatetime-day.md), tem um valor booliano especificado correspondente, como [**DaySpecified**](swbemdatetime-dayspecified.md). Quando **DaySpecified** é **false**, o valor é interpretado como um intervalo, em vez de um número entre 01 e 31. Se um intervalo for usado em qualquer lugar no valor de [data e hora](datetime.md) CIM, [**isinterval**](swbemdatetime-isinterval.md) também será definido como **true**. O padrão é que um valor DateTime de CIM contenha uma data em vez de um ou mais intervalos.

Por exemplo, se [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) for **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) incluirá o valor atual de [**SWbemDateTime. Day**](swbemdatetime-day.md), caso contrário, será um valor curinga. A propriedade [**isinterval**](swbemdatetime-isinterval.md) é **false** em ambos os casos.

## <a name="examples"></a>Exemplos

O exemplo de código de script a seguir mostra como usar um objeto **SWbemDateTime** para analisar um valor de propriedade DateTime lido no repositório WMI, a propriedade **InstallDate** no sistema [**\_ operacional Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



O exemplo a seguir mostra como criar um objeto **SWbemDateTime** , armazenar um valor de data no objeto, exibir a data como hora universal local e coordenada (UTC) e armazenar o valor em uma classe e propriedade recém-criadas. Para obter mais informações sobre a constante **wbemCimtypeDatetime**, consulte [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



O exemplo de código de script a seguir mostra como usar um objeto **SWbemDateTime** para modificar um valor de intervalo em uma propriedade que é lida no repositório WMI.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



O exemplo de código de script a seguir mostra como usar um objeto **SWbemDate** para ler um valor **FILETIME** .


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



O código do PowerShell a seguir cria uma instância de um objeto SWbemDateTime, recupera a data de instalação do sistema operacional e converte a data em um formato diferente


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



O código do PowerShell a seguir converte o código em um formato pronto para ser consumido por um provedor CIM.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



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

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[HORÁRIO](datetime.md)
</dt> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

