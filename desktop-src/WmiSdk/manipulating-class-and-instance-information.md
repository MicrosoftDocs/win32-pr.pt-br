---
description: O WMI fornece uma variedade de técnicas para recuperar e manipular informações de classe e instância do WMI, usando o Microsoft PowerShell, o Visual&\# 160; Basic Scripting Edition (VBScript) e C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipulando informações de classe e instância
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815470"
---
# <a name="manipulating-class-and-instance-information"></a><span data-ttu-id="a88fc-103">Manipulando informações de classe e instância</span><span class="sxs-lookup"><span data-stu-id="a88fc-103">Manipulating Class and Instance Information</span></span>

<span data-ttu-id="a88fc-104">O WMI fornece uma variedade de técnicas para recuperar e manipular informações de classe e instância do WMI, usando o Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) e C++.</span><span class="sxs-lookup"><span data-stu-id="a88fc-104">WMI provides a variety of techniques to retrieve and manipulate WMI class and instance information, using Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) and C++.</span></span>

<span data-ttu-id="a88fc-105">A tabela a seguir lista os tópicos que discutem as técnicas para recuperar e manipular informações de classe e instância do WMI.</span><span class="sxs-lookup"><span data-stu-id="a88fc-105">The following table lists the topics that discuss the techniques to retrieve and manipulate WMI class and instance information.</span></span>



| <span data-ttu-id="a88fc-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="a88fc-106">Topic</span></span>                                                                                  | <span data-ttu-id="a88fc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a88fc-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a88fc-108">Recuperando dados de instância ou classe WMI</span><span class="sxs-lookup"><span data-stu-id="a88fc-108">Retrieving WMI Class or Instance Data</span></span>](retrieving-class-or-instance-data.md)         | <span data-ttu-id="a88fc-109">Recuperar e definir dados de e para o repositório de informações do WMI.</span><span class="sxs-lookup"><span data-stu-id="a88fc-109">Retrieve and set data from and to the WMI information repository.</span></span>                                                                                                                 |
| [<span data-ttu-id="a88fc-110">Modificando uma propriedade de instância</span><span class="sxs-lookup"><span data-stu-id="a88fc-110">Modifying an Instance Property</span></span>](modifying-an-instance-property.md)                   | <span data-ttu-id="a88fc-111">Altere as informações na instância depois que ela for recuperada.</span><span class="sxs-lookup"><span data-stu-id="a88fc-111">Change the information in the instance after it is retrieved.</span></span>                                                                                                                     |
| [<span data-ttu-id="a88fc-112">Alterando a herança de uma instância</span><span class="sxs-lookup"><span data-stu-id="a88fc-112">Changing the Inheritance of an Instance</span></span>](changing-the-inheritance-of-an-instance.md) | <span data-ttu-id="a88fc-113">Altere a classe pai de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a88fc-113">Change the parent class of an instance.</span></span>                                                                                                                                           |
| [<span data-ttu-id="a88fc-114">Modificando um método</span><span class="sxs-lookup"><span data-stu-id="a88fc-114">Modifying a Method</span></span>](modifying-a-method.md)                                           | <span data-ttu-id="a88fc-115">Modifique os parâmetros de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a88fc-115">Modify the parameters of an instance.</span></span>                                                                                                                                             |
| [<span data-ttu-id="a88fc-116">Enumerando o WMI</span><span class="sxs-lookup"><span data-stu-id="a88fc-116">Enumerating WMI</span></span>](enumerating-wmi.md)                                                 | <span data-ttu-id="a88fc-117">Enumerar objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="a88fc-117">Enumerate WMI objects.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="a88fc-118">Consultando o WMI</span><span class="sxs-lookup"><span data-stu-id="a88fc-118">Querying WMI</span></span>](querying-wmi.md)                                                       | <span data-ttu-id="a88fc-119">Consultar objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="a88fc-119">Query WMI objects.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="a88fc-120">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="a88fc-120">Calling a Method</span></span>](calling-a-method.md)                                               | <span data-ttu-id="a88fc-121">Use os métodos associados criados pela Microsoft ou por outros desenvolvedores de terceiros para manipular mais objetos WMI ou, caso contrário, afetam diretamente o objeto que o objeto WMI representa.</span><span class="sxs-lookup"><span data-stu-id="a88fc-121">Use associated methods created by Microsoft or other third-party developers to further manipulate WMI objects, or else directly affect the object that the WMI object represents.</span></span> |
| [<span data-ttu-id="a88fc-122">Acessando uma coleção</span><span class="sxs-lookup"><span data-stu-id="a88fc-122">Accessing a Collection</span></span>](accessing-a-collection.md)                                   | <span data-ttu-id="a88fc-123">Enumere as coleções no script.</span><span class="sxs-lookup"><span data-stu-id="a88fc-123">Enumerate collections in script.</span></span>                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a><span data-ttu-id="a88fc-124">Manipulando dados usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a88fc-124">Manipulating Data Using VBScript</span></span>

<span data-ttu-id="a88fc-125">Você pode usar o acesso direto para acessar as propriedades WMI de uma instância ou classe WMI diretamente em um [**SWbemObject**](swbemobject.md), em vez de por meio da [coleção](accessing-a-collection.md) de propriedades desse objeto.</span><span class="sxs-lookup"><span data-stu-id="a88fc-125">You can use direct access to access the WMI properties of a WMI class or instance directly on an [**SWbemObject**](swbemobject.md), rather than through the property [collection](accessing-a-collection.md) of that object.</span></span> <span data-ttu-id="a88fc-126">Você também pode executar métodos nesse objeto no estilo nativo da linguagem de programação em vez de usar o [**SWbemServices.Exechamada cMethod**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="a88fc-126">You can also execute methods on that object in the native style of the programming language rather than using the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span> <span data-ttu-id="a88fc-127">Por exemplo, o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) no [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) tinha três parâmetros no Windows 2000, mas tem quatro parâmetros no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a88fc-127">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method in [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) had three parameters in Windows 2000 but has four parameters in Windows Server 2003.</span></span>

<span data-ttu-id="a88fc-128">Usando o acesso direto, você pode tratar Propriedades e métodos do WMI como se fossem Propriedades de automação e métodos de [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="a88fc-128">Using direct access, you can treat WMI properties and methods as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="a88fc-129">O exemplo a seguir mostra como você pode acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="a88fc-129">The following example shows how you can access a property.</span></span>


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



<span data-ttu-id="a88fc-130">O exemplo a seguir mostra como você pode acessar uma propriedade quando você tem acesso direto.</span><span class="sxs-lookup"><span data-stu-id="a88fc-130">The following example shows how you can access a property when you have direct access.</span></span>


```VB
VolumeName = MyDisk.VolumeName
```



<span data-ttu-id="a88fc-131">O encadeamento de objetos também é aceitável.</span><span class="sxs-lookup"><span data-stu-id="a88fc-131">Chaining of objects is also acceptable.</span></span>

<span data-ttu-id="a88fc-132">O exemplo a seguir mostra como acessar uma propriedade de um objeto inserido em outro objeto.</span><span class="sxs-lookup"><span data-stu-id="a88fc-132">The following example shows how to access a property of an object that is embedded in another object.</span></span>


```VB
value = MyComputer.MyDisk.VolumeName
```



<span data-ttu-id="a88fc-133">O exemplo a seguir mostra como acessar uma propriedade com a notação de subscrito de matriz.</span><span class="sxs-lookup"><span data-stu-id="a88fc-133">The following example shows how to access a property with array subscript notation.</span></span>


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



<span data-ttu-id="a88fc-134">O exemplo de código VBScript a seguir mostra como gerar uma instância dos parâmetros de entrada para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) na classe de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) como um [**SWbemObject**](swbemobject.md), preencher as propriedades de entrada e executar o método **Create** usando [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="a88fc-134">The following VBScript code example shows how to spawn an instance of the input parameters to the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method in the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class as an [**SWbemObject**](swbemobject.md), populate the input properties, and then execute the **Create** method using [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="a88fc-135">A propriedade [**SWbemObject. \_ Methods**](swbemobject-methods-.md) retorna uma coleção [**SWbemMethodSet**](swbemmethodset.md) dos métodos de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="a88fc-135">The [**SWbemObject.Methods\_**](swbemobject-methods-.md) property returns an [**SWbemMethodSet**](swbemmethodset.md) collection of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) methods.</span></span> <span data-ttu-id="a88fc-136">Os membros do conjunto de métodos são objetos [**SWbemMethod**](swbemmethod.md) e [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) retorna os parâmetros de entrada para o método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="a88fc-136">The members of the method set are [**SWbemMethod**](swbemmethod.md) objects and [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) returns the input parameters for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method.</span></span> <span data-ttu-id="a88fc-137">O parâmetro de entrada de *linha de comando* necessário está definido como "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="a88fc-137">The required *CommandLine* input parameter is set to "calc.exe".</span></span> <span data-ttu-id="a88fc-138">O método é executado por [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), resultando na inicialização de um processo de calc.exe.</span><span class="sxs-lookup"><span data-stu-id="a88fc-138">The method is then executed by [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), resulting in the launch of a calc.exe process.</span></span>


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



<span data-ttu-id="a88fc-139">O exemplo de código a seguir mostra como executar a operação anterior usando o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="a88fc-139">The following code example shows how to perform the previous operation using direct access.</span></span>


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



<span data-ttu-id="a88fc-140">Para obter mais informações, consulte [chamando um método de provedor](calling-a-provider-method.md) e [script com SWbemObject](scripting-with-swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="a88fc-140">For more information, see [Calling a Provider Method](calling-a-provider-method.md) and [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

 

 
