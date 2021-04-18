---
description: A exclusão de uma instância é o comando de exclusão mais comum que você provavelmente executará no WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Excluindo uma instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789321"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="f017c-103">Excluindo uma instância</span><span class="sxs-lookup"><span data-stu-id="f017c-103">Deleting an Instance</span></span>

<span data-ttu-id="f017c-104">A exclusão de uma instância é o comando de exclusão mais comum que você provavelmente executará no WMI.</span><span class="sxs-lookup"><span data-stu-id="f017c-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="f017c-105">Como excluir uma classe, o comando real é bem simples.</span><span class="sxs-lookup"><span data-stu-id="f017c-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="f017c-106">No entanto, o WMI é executado de forma muito diferente, dependendo do tipo de instância que você está excluindo.</span><span class="sxs-lookup"><span data-stu-id="f017c-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="f017c-107">Se a instância for estática, o WMI simplesmente excluirá a instância do repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="f017c-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="f017c-108">Para obter informações sobre como remover classes e instâncias do repositório do WMI, consulte o comando de pré-processador do [**pragma DeleteClass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="f017c-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="f017c-109">Se a instância for dinâmica, o WMI deverá chamar [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) nos provedores responsáveis pelas seguintes classes:</span><span class="sxs-lookup"><span data-stu-id="f017c-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="f017c-110">A classe que possui a instância.</span><span class="sxs-lookup"><span data-stu-id="f017c-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="f017c-111">Todas as classes pai da classe que possui a instância.</span><span class="sxs-lookup"><span data-stu-id="f017c-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="f017c-112">Todas as subclasses da classe que possui a instância.</span><span class="sxs-lookup"><span data-stu-id="f017c-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="f017c-113">O sucesso da exclusão depende da classe não abstrata mais alta para a instância original.</span><span class="sxs-lookup"><span data-stu-id="f017c-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="f017c-114">Se o provedor de qualquer classe não abstrata mais alta for concluído com sucesso ao concluir a exclusão, a operação terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="f017c-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="f017c-115">Para obter mais informações, consulte a seção comentários de [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="f017c-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="f017c-116">A [API com para WMI](com-api-for-wmi.md) tem métodos diferentes para excluir uma instância e excluir um objeto.</span><span class="sxs-lookup"><span data-stu-id="f017c-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="f017c-117">O procedimento a seguir descreve como usar o C++ para excluir uma instância de uma classe base ou classe derivada.</span><span class="sxs-lookup"><span data-stu-id="f017c-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="f017c-118">**Para excluir uma instância de uma classe base ou classe derivada usando C++**</span><span class="sxs-lookup"><span data-stu-id="f017c-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="f017c-119">Chame os métodos [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) ou [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="f017c-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="f017c-120">Como o nome sugere, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) exclui uma instância assincronamente enquanto [**deleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) exclui uma instância de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="f017c-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="f017c-121">Para usar o **DeleteInstanceAsync**, você também deve implementar um objeto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="f017c-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="f017c-122">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f017c-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f017c-123">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f017c-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="f017c-124">A [API de script para WMI](scripting-api-for-wmi.md) usa os mesmos métodos para excluir um objeto de classe ou uma instância.</span><span class="sxs-lookup"><span data-stu-id="f017c-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="f017c-125">O procedimento a seguir descreve como usar o VBScript para excluir uma instância de uma classe base ou classe derivada.</span><span class="sxs-lookup"><span data-stu-id="f017c-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="f017c-126">**Para excluir uma instância de uma classe base ou classe derivada usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="f017c-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="f017c-127">Chame os métodos [**SWbemObject. Delete \_**](swbemobject-delete-.md) ou [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="f017c-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="f017c-128">Como o nome sugere, [**delete \_**](swbemobject-delete-.md) exclui uma instância de forma síncrona enquanto [**DeleteAsync \_**](swbemobject-deleteasync-.md) exclui uma instância de maneira assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f017c-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="f017c-129">Para obter mais informações sobre como excluir uma instância de forma assíncrona, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f017c-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="f017c-130">O exemplo a seguir descreve como excluir uma instância usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="f017c-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="f017c-131">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f017c-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f017c-132">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f017c-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



