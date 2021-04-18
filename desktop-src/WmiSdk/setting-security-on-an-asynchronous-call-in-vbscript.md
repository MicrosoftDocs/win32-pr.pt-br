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
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a><span data-ttu-id="549a0-103">Definindo a segurança em uma chamada assíncrona no VBScript</span><span class="sxs-lookup"><span data-stu-id="549a0-103">Setting Security on an Asynchronous Call in VBScript</span></span>

<span data-ttu-id="549a0-104">O desempenho das chamadas [*semisynchronous*](gloss-s.md) é geralmente adequado para a maioria das situações.</span><span class="sxs-lookup"><span data-stu-id="549a0-104">The performance of [*semisynchronous*](gloss-s.md) calls is usually adequate for most situations.</span></span> <span data-ttu-id="549a0-105">Chamadas assíncronas geralmente não são uma prática recomendada para scripts.</span><span class="sxs-lookup"><span data-stu-id="549a0-105">Asynchronous calls are generally not a recommended practice for scripts.</span></span> <span data-ttu-id="549a0-106">No entanto, se for necessário fazer chamadas assíncronas, um valor de registro poderá ser definido para forçar o WMI a executar verificações de acesso em chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="549a0-106">However, if asynchronous calls must be made, a registry value can be set to force WMI to perform access checks on asynchronous calls.</span></span>


<span data-ttu-id="549a0-107">O valor do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla se o WMI verifica um nível de autenticação aceitável ao retornar dados para uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="549a0-107">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level when returning data for an asynchronous call.</span></span> <span data-ttu-id="549a0-108">O retorno de chamada pode ser retornado em um nível de autenticação inferior ao da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="549a0-108">The callback can be returned at a lower authentication level than that of the original asynchronous call.</span></span> <span data-ttu-id="549a0-109">Por padrão, esse valor é definido como zero para que os retornos de chamada não sejam verificados.</span><span class="sxs-lookup"><span data-stu-id="549a0-109">By default, this value is set to zero so that callbacks are not checked.</span></span> <span data-ttu-id="549a0-110">Para proteger chamadas assíncronas em scripts, você deve definir a chave do registro como 1 (uma).</span><span class="sxs-lookup"><span data-stu-id="549a0-110">To secure asynchronous calls in scripting, you must set the registry key to 1 (one).</span></span>

<span data-ttu-id="549a0-111">Os scripts podem usar os métodos [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) do objeto Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para alterar a configuração do valor do registro **UnsecAppAccessControlDefault** .</span><span class="sxs-lookup"><span data-stu-id="549a0-111">Scripts can use the [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) methods of the registry object [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) to change the setting of the **UnsecAppAccessControlDefault** registry value.</span></span> <span data-ttu-id="549a0-112">Para obter mais informações sobre os níveis de autenticação e representação necessários para o acesso remoto, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="549a0-112">For more information about authentication and impersonation levels required for remote access, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-set-asynchronous-call-security-in-vbscript"></a><span data-ttu-id="549a0-113">Para definir a segurança de chamada assíncrona no VBScript</span><span class="sxs-lookup"><span data-stu-id="549a0-113">To set asynchronous call security in VBScript</span></span>

<span data-ttu-id="549a0-114">O exemplo de código VBScript a seguir mostra como alterar o valor do registro para controlar a autenticação WMI de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="549a0-114">The following VBScript code example shows you how to change the registry value to control WMI authentication of callbacks.</span></span>

<span data-ttu-id="549a0-115">O script altera o valor de **UnsecAppAccessControlDefault** de zero para um, ou se o valor já estiver definido, de um para zero.</span><span class="sxs-lookup"><span data-stu-id="549a0-115">The script changes the value of **UnsecAppAccessControlDefault** from zero to one, or if the value is already set, from one to zero.</span></span> <span data-ttu-id="549a0-116">Zero é o padrão em um sistema recentemente instalado.</span><span class="sxs-lookup"><span data-stu-id="549a0-116">Zero is the default on a newly installed system.</span></span> <span data-ttu-id="549a0-117">Depois que o sinalizador é definido, a configuração persiste na reinicialização ou na reinicialização do WMI.</span><span class="sxs-lookup"><span data-stu-id="549a0-117">Once the flag is set, the setting persists across reboot or WMI restart.</span></span>

<span data-ttu-id="549a0-118">O script usa um objeto [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) e [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) para chamar [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="549a0-118">The script uses a [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) object and [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) to call [**StdRegProv.GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span> <span data-ttu-id="549a0-119">Para obter mais informações sobre como definir os valores em um objeto de **inparâmetros** , consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="549a0-119">For more information about setting the values in an **InParameters** object, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="549a0-120">Para obter um exemplo de uma chamada de registro usando [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), consulte [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="549a0-120">For an example of a registry call using [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), see [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span>


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



 

 
