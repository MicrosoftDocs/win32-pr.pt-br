---
description: Um objeto de inparâmetros contém a lista de parâmetros para chamar métodos de provedor ao usar um tipo de chamada de ExecMethod.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Construindo objetos de inparâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827847"
---
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="70b5c-103">Construindo objetos de inparâmetros</span><span class="sxs-lookup"><span data-stu-id="70b5c-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="70b5c-104">Um objeto de [**inparâmetros**](swbemmethod-inparameters.md) contém a lista de parâmetros para chamar métodos de provedor ao usar um tipo de chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="70b5c-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="70b5c-105">Os métodos [**SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) requerem um objeto de **inparâmetros** .</span><span class="sxs-lookup"><span data-stu-id="70b5c-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="70b5c-106">O procedimento a seguir descreve como construir um objeto de [**inparâmetros**](swbemmethod-inparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="70b5c-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="70b5c-107">**Para construir o parâmetro *objwbemInParams***</span><span class="sxs-lookup"><span data-stu-id="70b5c-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="70b5c-108">Conecte-se ao WMI.</span><span class="sxs-lookup"><span data-stu-id="70b5c-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="70b5c-109">Obtenha a definição da classe WMI que define o método que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="70b5c-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="70b5c-110">Obtenha um objeto de [**inparâmetros**](swbemmethod-inparameters.md) específico para o método de classe WMI que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="70b5c-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="70b5c-111">Defina as propriedades da instância para quaisquer valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="70b5c-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="70b5c-112">Certifique-se de atribuir valores às propriedades de chave na classe WMI que contém o método que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="70b5c-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="70b5c-113">Por exemplo, se você quiser definir um parâmetro de entrada chamado myinputparam para o valor "ABC" em uma instância de [**inparâmetros**](swbemmethod-inparameters.md) chamada "Inst", o código ficaria assim.</span><span class="sxs-lookup"><span data-stu-id="70b5c-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="70b5c-114">Execute o método e obtenha o status de retorno do método que você está executando.</span><span class="sxs-lookup"><span data-stu-id="70b5c-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="70b5c-115">O exemplo de código a seguir ilustra a configuração do objeto [**Parameters**](swbemmethod-inparameters.md) para criar um novo objeto WMI que representa um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="70b5c-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="70b5c-116">Para obter mais informações sobre o objeto [**Parameters**](swbemmethod-outparameters.md) , consulte [analisando objetos de Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="70b5c-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="70b5c-117">Este exemplo retorna um valor de retorno com êxito (0) se houver uma pasta chamada "compartilhamento" no local "C:/compartilhamento".</span><span class="sxs-lookup"><span data-stu-id="70b5c-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="70b5c-118">Este exemplo permite que essa pasta seja compartilhada com outros usuários.</span><span class="sxs-lookup"><span data-stu-id="70b5c-118">This example enables this folder to be shared with other users.</span></span>


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



