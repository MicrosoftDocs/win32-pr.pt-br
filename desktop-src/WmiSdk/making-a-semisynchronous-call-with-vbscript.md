---
description: Fornece a funcionalidade de acesso do semisynchronous e um exemplo de código para fazer uma chamada de método semisynchronous.
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: Fazendo uma chamada Semisynchronous com o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790478"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="56d46-103">Fazendo uma chamada Semisynchronous com o VBScript</span><span class="sxs-lookup"><span data-stu-id="56d46-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="56d46-104">Alguns métodos WMI podem retornar grandes coleções, fazendo com que os scripts parem de responder.</span><span class="sxs-lookup"><span data-stu-id="56d46-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="56d46-105">No script, o acesso semisynchronous é o padrão, e instrumentação de gerenciamento do Windows (WMI) define **wbemFlagReturnImmediately** para chamadas que podem retornar grandes coleções de objetos, como os seguintes métodos [**SWbemServices**](swbemservices.md) : [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md)e [**References**](swbemservices-referencesto.md).</span><span class="sxs-lookup"><span data-stu-id="56d46-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="56d46-106">O acesso Semisynchronous que usa **wbemFlagReturnImmediately** definido no parâmetro *iFlags* também é o padrão para chamadas que podem retornar grandes conjuntos de objetos para os seguintes métodos [**SWbemObject**](swbemobject.md) : [**instâncias \_**](swbemobject-instances-.md), [**subclasses \_**](swbemobject-subclasses-.md), [**ASSOCIADORES \_**](swbemobject-associators-.md)e [**referências \_**](swbemobject-references-.md).</span><span class="sxs-lookup"><span data-stu-id="56d46-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="56d46-107">Para reduzir o uso de recursos de memória WMI ao processar uma grande coleção de objetos, inclua o valor de **wbemFlagForwardOnly** no parâmetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="56d46-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="56d46-108">O uso de **wbemFlagForwardOnly** faz com que o WMI crie um enumerador somente de encaminhamento que não permite rebobinar a coleção e acessar itens novamente.</span><span class="sxs-lookup"><span data-stu-id="56d46-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="56d46-109">O WMI elimina a memória de cada objeto, uma vez que a instrução **for each** processa um objeto.</span><span class="sxs-lookup"><span data-stu-id="56d46-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="56d46-110">Você não pode chamar o método **Count** para uma coleção quando o sinalizador **wbemFlagForwardOnly** foi definido na chamada que obteve a coleção.</span><span class="sxs-lookup"><span data-stu-id="56d46-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="56d46-111">Observe que o parâmetro *iFlags* tem **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** definidos por padrão para o método [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="56d46-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="56d46-112">O procedimento a seguir descreve como usar o VBScript para fazer uma chamada semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="56d46-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="56d46-113">**Para fazer uma chamada semisynchronous no VBScript**</span><span class="sxs-lookup"><span data-stu-id="56d46-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="56d46-114">Defina o parâmetro *iFlags* para o valor de [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="56d46-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="56d46-115">Faça a chamada síncrona normal para [**SWbemServices.ExecQuery**](swbemservices-execquery.md) ou [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) com o valor *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="56d46-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="56d46-116">Se você quiser tratar os objetos retornados pela chamada como uma coleção, use uma sintaxe de enumeração como VBScript **para cada** um.</span><span class="sxs-lookup"><span data-stu-id="56d46-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="56d46-117">À medida que cada objeto é retornado, ele é processado como o próximo item da coleção.</span><span class="sxs-lookup"><span data-stu-id="56d46-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="56d46-118">Crie um enumerador somente encaminhamento combinando o valor de **wbemFlagReturnImmediately** com o valor de **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="56d46-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="56d46-119">O valor decimal dessa operação ou é 48.</span><span class="sxs-lookup"><span data-stu-id="56d46-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="56d46-120">Essas constantes são definidas na biblioteca de tipos wbemdisp. tlb para Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="56d46-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="56d46-121">A maioria das linguagens de script usa o valor numérico ou define uma constante.</span><span class="sxs-lookup"><span data-stu-id="56d46-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="56d46-122">Para obter mais informações, consulte [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="56d46-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="56d46-123">O exemplo de código a seguir mostra como fazer uma chamada de método semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="56d46-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="56d46-124">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="56d46-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="56d46-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56d46-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56d46-126">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="56d46-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



