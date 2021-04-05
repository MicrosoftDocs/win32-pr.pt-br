---
description: Normalmente, o acesso direto é adequado para chamar um método de provedor WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construindo objetos de inparâmetros e analisando objetos de Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922202"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="eac26-103">Construindo objetos de inparâmetros e analisando objetos de Parameters</span><span class="sxs-lookup"><span data-stu-id="eac26-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="eac26-104">Normalmente, o acesso direto é adequado para chamar um [*método de provedor*](gloss-p.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="eac26-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="eac26-105">Acesso direto significa executar um método usando a sintaxe *Object. Method* .</span><span class="sxs-lookup"><span data-stu-id="eac26-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="eac26-106">No entanto, em alguns casos, o acesso direto não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="eac26-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="eac26-107">Além disso, chamar um método de provedor de forma assíncrona de um script requer um tipo de chamada [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="eac26-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="eac26-108">Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="eac26-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="eac26-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eac26-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="eac26-110">A ordem dos parâmetros de entrada e saída do método é definida no esquema formato MOF (MOF) para o método.</span><span class="sxs-lookup"><span data-stu-id="eac26-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="eac26-111">O WMI não impede que a ordem do parâmetro seja alterada quando a classe é recompilada pelo [Mofcomp](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="eac26-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="eac26-112">Usando um objeto de [**inparâmetros**](swbemmethod-inparameters.md) , você pode evitar problemas resultantes do esquema alterado porque os parâmetros de entrada são identificados por nome.</span><span class="sxs-lookup"><span data-stu-id="eac26-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="eac26-113">O parâmetro correto pode ser visto examinando o qualificador de **ID** de cada parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="eac26-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="eac26-114">O primeiro parâmetro tem um valor de **ID** igual a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="eac26-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="eac26-115">[**Os métodos SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) fornecem uma maneira alternativa de executar um método de provedor em casos em que não é possível executar um método diretamente.</span><span class="sxs-lookup"><span data-stu-id="eac26-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="eac26-116">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="eac26-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="eac26-117">Para obter mais informações sobre parâmetros, consulte [construindo objetos de inparâmetros](constructing-inparameters-objects.md) e [analisando objetos de Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eac26-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



