---
description: O desempenho das chamadas semisynchronous é geralmente adequado para a maioria das situações.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Definindo a segurança em uma chamada assíncrona no VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811717"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Definindo a segurança em uma chamada assíncrona no VBScript

O desempenho das chamadas [*semisynchronous*](gloss-s.md) é geralmente adequado para a maioria das situações. Chamadas assíncronas geralmente não são uma prática recomendada para scripts. No entanto, se for necessário fazer chamadas assíncronas, um valor de registro poderá ser definido para forçar o WMI a executar verificações de acesso em chamadas assíncronas.


O valor do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla se o WMI verifica um nível de autenticação aceitável ao retornar dados para uma chamada assíncrona. O retorno de chamada pode ser retornado em um nível de autenticação inferior ao da chamada assíncrona original. Por padrão, esse valor é definido como zero para que os retornos de chamada não sejam verificados. Para proteger chamadas assíncronas em scripts, você deve definir a chave do registro como 1 (uma).

Os scripts podem usar os métodos [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) do objeto Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para alterar a configuração do valor do registro **UnsecAppAccessControlDefault** . Para obter mais informações sobre os níveis de autenticação e representação necessários para o acesso remoto, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>Para definir a segurança de chamada assíncrona no VBScript

O exemplo de código VBScript a seguir mostra como alterar o valor do registro para controlar a autenticação WMI de retornos de chamada.

O script altera o valor de **UnsecAppAccessControlDefault** de zero para um, ou se o valor já estiver definido, de um para zero. Zero é o padrão em um sistema recentemente instalado. Depois que o sinalizador é definido, a configuração persiste na reinicialização ou na reinicialização do WMI.

O script usa um objeto [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) e [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) para chamar [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov). Para obter mais informações sobre como definir os valores em um objeto de **inparâmetros** , consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Para obter um exemplo de uma chamada de registro usando [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), consulte [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
