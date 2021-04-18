---
description: Se você estiver usando a API de script para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade como parte de um moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Recuperando classes corrigidas usando a API de script para WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771562"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="f08e6-103">Recuperando classes corrigidas usando a API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="f08e6-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="f08e6-104">Se você estiver usando a API de script para que o WMI recupere ou armazene informações de classe localizadas, especifique a localidade como parte de um moniker.</span><span class="sxs-lookup"><span data-stu-id="f08e6-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="f08e6-105">Ou, você pode fornecer o nome da localidade no parâmetro *strLocale* para o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f08e6-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="f08e6-106">Ao ler ou gravar classes corrigidas, indique que você deseja usar definições de classe localizadas especificando [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) como um sinalizador para o parâmetro *iFlags* do método que você chama.</span><span class="sxs-lookup"><span data-stu-id="f08e6-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="f08e6-107">Para o PowerShell, você pode usar o parâmetro *-locale* em [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) para especificar a localidade.</span><span class="sxs-lookup"><span data-stu-id="f08e6-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="f08e6-108">O exemplo de código a seguir mostra como recuperar uma classe localizada usando um moniker scripting do WMI ou o parâmetro-locale.</span><span class="sxs-lookup"><span data-stu-id="f08e6-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="f08e6-109">O exemplo de código a seguir mostra como definir o parâmetro locale e usar o sinalizador [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="f08e6-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="f08e6-110">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f08e6-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f08e6-111">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f08e6-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="f08e6-112">A tabela a seguir lista os métodos que aceitam o sinalizador [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="f08e6-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="f08e6-113">Método síncrono</span><span class="sxs-lookup"><span data-stu-id="f08e6-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="f08e6-114">Método assíncrono</span><span class="sxs-lookup"><span data-stu-id="f08e6-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f08e6-115">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="f08e6-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="f08e6-116">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="f08e6-117">**Subclasses de SWbemObject\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="f08e6-118">**SWbemObject. SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="f08e6-119">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="f08e6-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="f08e6-120">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="f08e6-121">**SWbemObject. instâncias\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="f08e6-122">**SWbemObject. InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="f08e6-123">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="f08e6-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="f08e6-124">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="f08e6-125">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="f08e6-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="f08e6-126">**SWbemServices. getasync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="f08e6-127">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="f08e6-128">**SWbemObject. PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="f08e6-129">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="f08e6-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="f08e6-130">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="f08e6-131">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="f08e6-132">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="f08e6-133">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="f08e6-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="f08e6-134">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="f08e6-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="f08e6-135">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="f08e6-136">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="f08e6-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
