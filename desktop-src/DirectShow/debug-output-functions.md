---
description: Funções de saída de depuração
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funções de saída de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105750031"
---
# <a name="debug-output-functions"></a><span data-ttu-id="067fe-103">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="067fe-103">Debug Output Functions</span></span>

<span data-ttu-id="067fe-104">As [classes base do DirectShow](directshow-base-classes.md) fornecem várias macros para exibir informações de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="067fe-105">Função</span><span class="sxs-lookup"><span data-stu-id="067fe-105">Function</span></span>                                               | <span data-ttu-id="067fe-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="067fe-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="067fe-107">**DbgCheckModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="067fe-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="067fe-108">Verifica se o log está habilitado para os tipos e o nível de mensagem fornecidos.</span><span class="sxs-lookup"><span data-stu-id="067fe-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="067fe-109">**DbgDumpObjectRegister**</span><span class="sxs-lookup"><span data-stu-id="067fe-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="067fe-110">Exibe informações sobre objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="067fe-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="067fe-111">**DbgInitialise**</span><span class="sxs-lookup"><span data-stu-id="067fe-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="067fe-112">Inicializa a biblioteca de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="067fe-113">**DbgLog**</span><span class="sxs-lookup"><span data-stu-id="067fe-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="067fe-114">Envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados.</span><span class="sxs-lookup"><span data-stu-id="067fe-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="067fe-115">**DbgOutString**</span><span class="sxs-lookup"><span data-stu-id="067fe-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="067fe-116">Envia uma cadeia de caracteres para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="067fe-117">**DbgSetModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="067fe-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="067fe-118">Define o nível de log para um ou mais tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="067fe-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="067fe-119">**DbgTerminate**</span><span class="sxs-lookup"><span data-stu-id="067fe-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="067fe-120">Limpa a biblioteca de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="067fe-121">**TipoDeExibição**</span><span class="sxs-lookup"><span data-stu-id="067fe-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="067fe-122">Envia informações sobre um tipo de mídia para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="067fe-123">**DumpGraph**</span><span class="sxs-lookup"><span data-stu-id="067fe-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="067fe-124">Envia informações sobre um grafo de filtro para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="067fe-125">**GuidNames**</span><span class="sxs-lookup"><span data-stu-id="067fe-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="067fe-126">Matriz global que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="067fe-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="067fe-127">**NOMES**</span><span class="sxs-lookup"><span data-stu-id="067fe-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="067fe-128">Gera uma cadeia de caracteres somente depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="067fe-129">**ANOTAÇÕES**</span><span class="sxs-lookup"><span data-stu-id="067fe-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="067fe-130">Envia uma cadeia de caracteres para o local de saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="067fe-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="067fe-131">**-**</span><span class="sxs-lookup"><span data-stu-id="067fe-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="067fe-132">Gera um lembrete no tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="067fe-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="067fe-133">**Chaves do registro**</span><span class="sxs-lookup"><span data-stu-id="067fe-133">**Registry Keys**</span></span>

<span data-ttu-id="067fe-134">A função Debug Output no DirectShow usa um conjunto de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="067fe-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="067fe-135">O local dessas chaves do registro depende da versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="067fe-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="067fe-136">*Antes do Windows Vista*, as chaves de depuração estão localizadas no seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="067fe-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="067fe-137">**HKEY \_ \_** Depuração de \\ **software** \\  de computador local</span><span class="sxs-lookup"><span data-stu-id="067fe-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="067fe-138">No Windows Vista ou posterior, eles estão localizados no seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="067fe-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="067fe-139">**HKEY \_ \_Computador local** \\ **software** de \\  \\  \\ **depuração** do Microsoft DirectShow</span><span class="sxs-lookup"><span data-stu-id="067fe-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="067fe-140">Para filtros de terceiros, o local depende de qual versão das [classes base do DirectShow](directshow-base-classes.md) foi usada para criar o filtro.</span><span class="sxs-lookup"><span data-stu-id="067fe-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="067fe-141">A versão incluída no SDK do Windows para o Windows Vista usa o caminho mais recente.</span><span class="sxs-lookup"><span data-stu-id="067fe-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="067fe-142">As versões anteriores usaram o caminho mais antigo.</span><span class="sxs-lookup"><span data-stu-id="067fe-142">Previous versions used the older path.</span></span>

<span data-ttu-id="067fe-143">Nos comentários a seguir, o rótulo *<DebugRoot>* é usado para indicar esses dois caminhos.</span><span class="sxs-lookup"><span data-stu-id="067fe-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="067fe-144">Substitua o caminho correto, dependendo da versão do Windows ou da versão das classes base.</span><span class="sxs-lookup"><span data-stu-id="067fe-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="067fe-145">**Log de depuração**</span><span class="sxs-lookup"><span data-stu-id="067fe-145">**Debug Logging**</span></span>

<span data-ttu-id="067fe-146">O DirectShow define vários tipos de mensagem, mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="067fe-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="067fe-147">Valor</span><span class="sxs-lookup"><span data-stu-id="067fe-147">Value</span></span>                   | <span data-ttu-id="067fe-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="067fe-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="067fe-149">erro de LOG \_</span><span class="sxs-lookup"><span data-stu-id="067fe-149">LOG\_ERROR</span></span>              | <span data-ttu-id="067fe-150">Notificação de erro.</span><span class="sxs-lookup"><span data-stu-id="067fe-150">Error notification.</span></span>                                     |
| <span data-ttu-id="067fe-151">bloqueio de LOG \_</span><span class="sxs-lookup"><span data-stu-id="067fe-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="067fe-152">Bloqueio e desbloqueio de seções críticas.</span><span class="sxs-lookup"><span data-stu-id="067fe-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="067fe-153">memória de LOG \_</span><span class="sxs-lookup"><span data-stu-id="067fe-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="067fe-154">Alocação de memória e criação e destruição de objetos.</span><span class="sxs-lookup"><span data-stu-id="067fe-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="067fe-155">tempo de LOG \_</span><span class="sxs-lookup"><span data-stu-id="067fe-155">LOG\_TIMING</span></span>             | <span data-ttu-id="067fe-156">Medições de tempo e desempenho.</span><span class="sxs-lookup"><span data-stu-id="067fe-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="067fe-157">rastreamento de LOG \_</span><span class="sxs-lookup"><span data-stu-id="067fe-157">LOG\_TRACE</span></span>              | <span data-ttu-id="067fe-158">Rastreamento de chamada geral.</span><span class="sxs-lookup"><span data-stu-id="067fe-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="067fe-159">PERSONALIZADO1 por meio de CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="067fe-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="067fe-160">Disponível para mensagens de depuração personalizadas</span><span class="sxs-lookup"><span data-stu-id="067fe-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="067fe-161">Cada uma das funções de log de depuração do DirectShow especifica um tipo de mensagem e um nível de log.</span><span class="sxs-lookup"><span data-stu-id="067fe-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="067fe-162">A mensagem de depuração é exibida somente quando o nível de depuração atual para esse tipo de mensagem é igual ou maior que o nível especificado na função de log.</span><span class="sxs-lookup"><span data-stu-id="067fe-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="067fe-163">Caso contrário, a mensagem será ignorada.</span><span class="sxs-lookup"><span data-stu-id="067fe-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="067fe-164">Por exemplo, o código a seguir gera a cadeia de caracteres "esta é uma mensagem de depuração" se o nível de rastreamento de LOG \_ for 3 ou superior:</span><span class="sxs-lookup"><span data-stu-id="067fe-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="067fe-165">Cada módulo pode definir seu próprio nível de depuração para cada tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="067fe-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="067fe-166">(Um *módulo* é uma DLL ou um executável que pode ser carregado usando a função **LoadLibrary** .) Os níveis de depuração de um módulo aparecem no registro na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="067fe-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="067fe-167">**\_máquina local \_ HKEY**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="067fe-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="067fe-168">em que *<Message Type>* é o tipo de mensagem menos o "log \_ " inicial; por exemplo, **bloqueio** para mensagens de bloqueio de log \_ .</span><span class="sxs-lookup"><span data-stu-id="067fe-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="067fe-169">Quando um módulo é carregado, a biblioteca de depuração localiza os níveis de log do módulo no registro.</span><span class="sxs-lookup"><span data-stu-id="067fe-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="067fe-170">Se as chaves do registro não existirem, a biblioteca de depuração as criará.</span><span class="sxs-lookup"><span data-stu-id="067fe-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="067fe-171">Um módulo também pode definir seus próprios níveis em tempo de execução, usando a função [**DbgSetModuleLevel**](dbgsetmodulelevel.md) .</span><span class="sxs-lookup"><span data-stu-id="067fe-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="067fe-172">Para enviar uma mensagem para a saída de depuração, chame a macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="067fe-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="067fe-173">O exemplo a seguir cria uma mensagem de nível 3 do tipo rastreamento de LOG \_ :</span><span class="sxs-lookup"><span data-stu-id="067fe-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="067fe-174">Você também pode especificar níveis de log globais, com a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="067fe-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="067fe-175">A biblioteca de depuração usa qualquer nível que seja maior, o nível global ou o nível de módulo.</span><span class="sxs-lookup"><span data-stu-id="067fe-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="067fe-176">**Local de saída de depuração**</span><span class="sxs-lookup"><span data-stu-id="067fe-176">**Debug Output Location**</span></span>

<span data-ttu-id="067fe-177">O local de saída de depuração é determinado por outra chave do registro:</span><span class="sxs-lookup"><span data-stu-id="067fe-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="067fe-178">**HKEY \_ \_Máquina local** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**</span><span class="sxs-lookup"><span data-stu-id="067fe-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="067fe-179">Se o valor dessa chave for `Console` , a saída vai para a janela do console.</span><span class="sxs-lookup"><span data-stu-id="067fe-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="067fe-180">Se o valor for `Deb` , `Debug` , `Debugger` ou uma cadeia de caracteres vazia, a saída vai para a janela do depurador.</span><span class="sxs-lookup"><span data-stu-id="067fe-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="067fe-181">Caso contrário, a saída será gravada em um arquivo especificado pela chave do registro.</span><span class="sxs-lookup"><span data-stu-id="067fe-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="067fe-182">Antes que um executável use a biblioteca de depuração do DirectShow, ele deve chamar a função [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="067fe-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="067fe-183">Depois disso, ele deve chamar a função [**DbgTerminate**](dbgterminate.md) .</span><span class="sxs-lookup"><span data-stu-id="067fe-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="067fe-184">As DLLs não precisam chamar essas funções, porque o ponto de entrada de DLL (definido na biblioteca de classes base) as chama automaticamente.</span><span class="sxs-lookup"><span data-stu-id="067fe-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="067fe-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="067fe-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="067fe-186">Utilitários de depuração</span><span class="sxs-lookup"><span data-stu-id="067fe-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



