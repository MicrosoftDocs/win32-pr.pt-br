---
description: Muitos dos recursos de depuração descritos neste tópico são implementados na biblioteca de classes base do DirectShow. Para obter mais informações, consulte classes base do DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Depuração de filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500676"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="bc6a1-104">Depuração de filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc6a1-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="bc6a1-105">Muitos dos recursos de depuração descritos neste tópico são implementados na biblioteca de classes base do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="bc6a1-106">Para obter mais informações, consulte [classes base do DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="bc6a1-107">Verificação de asserção</span><span class="sxs-lookup"><span data-stu-id="bc6a1-107">Assertion Checking</span></span>

<span data-ttu-id="bc6a1-108">Use a verificação de asserção livremente.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-108">Use assertion checking liberally.</span></span> <span data-ttu-id="bc6a1-109">As asserções podem verificar suposições que você faz em seu código sobre pré-condições e pré-condições.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="bc6a1-110">O DirectShow fornece várias macros de asserção.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="bc6a1-111">Para obter mais informações, consulte [declarações e macros de ponto de interrupção](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="bc6a1-112">Nomes de objeto</span><span class="sxs-lookup"><span data-stu-id="bc6a1-112">Object Names</span></span>

<span data-ttu-id="bc6a1-113">Em compilações de depuração, há uma lista global de objetos que derivam da classe [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6a1-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="bc6a1-114">À medida que os objetos são criados, eles são adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="bc6a1-115">Quando eles são destruídos, eles são removidos da lista.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="bc6a1-116">Para exibir uma lista desses objetos, chame a função [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6a1-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="bc6a1-117">O método de construtor para a classe base [**CBaseObject**](cbaseobject.md) — e a maioria das classes derivadas dela — inclui um parâmetro para o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="bc6a1-118">Dê aos seus objetos nomes exclusivos para identificá-los.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="bc6a1-119">Use a macro [**Name**](name.md) quando você declarar o nome, de modo que o nome seja alocado somente em builds de depuração.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="bc6a1-120">Em compilações de varejo, o nome se torna **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="bc6a1-121">Log de depuração</span><span class="sxs-lookup"><span data-stu-id="bc6a1-121">Debug Logging</span></span>

<span data-ttu-id="bc6a1-122">A função [**DbgLog**](dbglog.md) exibe mensagens de depuração à medida que seu programa é executado.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="bc6a1-123">Use essa função para rastrear a execução do seu aplicativo ou filtro.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="bc6a1-124">Você pode registrar códigos de retorno, os valores de variáveis e quaisquer outras informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="bc6a1-125">Cada mensagem de depuração tem um tipo, como rastreamento de LOG \_ ou \_ erro de log, e um nível de depuração, que indica a importância da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="bc6a1-126">As mensagens com níveis inferiores de depuração são mais importantes do que aquelas com níveis mais altos.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="bc6a1-127">No exemplo a seguir, um filtro hipotético desconecta um PIN de uma matriz de Pins.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="bc6a1-128">Se a tentativa de desconexão for realizada com sucesso, o filtro exibirá uma mensagem de rastreamento de LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="bc6a1-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="bc6a1-129">Se a tentativa falhar, ela exibirá uma \_ mensagem de erro de log:</span><span class="sxs-lookup"><span data-stu-id="bc6a1-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="bc6a1-130">Ao depurar, você pode definir o nível de depuração para cada tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="bc6a1-131">Além disso, cada módulo (DLL ou executável) mantém seus próprios níveis de depuração.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="bc6a1-132">Se você estiver testando um filtro, gere os níveis de depuração para a DLL que contém o filtro.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="bc6a1-133">Para obter mais informações, consulte [depurar funções de saída](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="bc6a1-134">Seções críticas</span><span class="sxs-lookup"><span data-stu-id="bc6a1-134">Critical Sections</span></span>

<span data-ttu-id="bc6a1-135">Para facilitar o controle dos deadlocks, inclua as asserções que determinam se o código de chamada possui uma determinada seção crítica.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="bc6a1-136">As funções [**CritCheckIn**](critcheckin.md) e [**CritCheckOut**](critcheckout.md) indicam se o thread de chamada possui uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="bc6a1-137">Normalmente, você chamaria essas funções de dentro de uma macro Assert.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="bc6a1-138">Você também pode usar a função [**DbgLockTrace**](dbglocktrace.md) para rastrear quando seções críticas são mantidas ou liberadas.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc6a1-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc6a1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc6a1-140">Depuração no DirectShow</span><span class="sxs-lookup"><span data-stu-id="bc6a1-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



