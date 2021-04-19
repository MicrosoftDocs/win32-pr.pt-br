---
description: O utilitário de linha de comando do WMI (WMIC) fornece uma interface de linha de comando para o WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222924"
---
# <a name="wmic"></a><span data-ttu-id="b6e2d-103">wmic</span><span class="sxs-lookup"><span data-stu-id="b6e2d-103">wmic</span></span>

<span data-ttu-id="b6e2d-104">O utilitário de linha de comando do WMI (WMIC) fornece uma interface de linha de comando para Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="b6e2d-105">O WMIC é compatível com shells e comandos de utilitário existentes.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="b6e2d-106">Veja a seguir um tópico de referência geral para o WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="b6e2d-107">Para obter mais informações e diretrizes sobre como usar o WMIC, incluindo informações adicionais sobre aliases, verbos, switches e comandos, consulte [usando instrumentação de gerenciamento do Windows linha de comando](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) e [WMIC – use o controle de linha de comando sobre o WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="b6e2d-108">Alias</span><span class="sxs-lookup"><span data-stu-id="b6e2d-108">Alias</span></span>

<span data-ttu-id="b6e2d-109">Um alias é uma renomeação amigável de uma classe, propriedade ou método que torna o WMI mais fácil de usar e ler.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="b6e2d-110">Você pode determinar quais aliases estão disponíveis para WMIC por meio do **/?**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="b6e2d-111">.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-111">command.</span></span> <span data-ttu-id="b6e2d-112">Você também pode determinar os aliases para uma classe específica usando o **<className> /?**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="b6e2d-113">.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-113">command.</span></span> <span data-ttu-id="b6e2d-114">Para obter mais informações, consulte [aliases do WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="b6e2d-115">Comutador</span><span class="sxs-lookup"><span data-stu-id="b6e2d-115">Switch</span></span>

<span data-ttu-id="b6e2d-116">Um comutador é uma opção WMIC que pode ser definida globalmente ou opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="b6e2d-117">Para obter uma lista de opções disponíveis, consulte [Opções de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="b6e2d-118">Verbos</span><span class="sxs-lookup"><span data-stu-id="b6e2d-118">Verbs</span></span>

<span data-ttu-id="b6e2d-119">Para usar verbos no WMIC, insira o nome do alias seguido pelo verbo.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="b6e2d-120">Se um alias não oferecer suporte a um verbo, você receberá a mensagem "o provedor não é capaz da operação tentada".</span><span class="sxs-lookup"><span data-stu-id="b6e2d-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="b6e2d-121">Para obter mais informações, consulte [verbos do WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="b6e2d-122">A maioria dos aliases dá suporte aos verbos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="b6e2d-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOCIAÇÕES</span><span class="sxs-lookup"><span data-stu-id="b6e2d-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-124">Retorna o resultado da `Associators of (<wmi_object>)` consulta em que *<\_ objeto WMI>* é o caminho dos objetos retornados pelos comandos de **classe** ou **caminho** .</span><span class="sxs-lookup"><span data-stu-id="b6e2d-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="b6e2d-125">Os resultados são instâncias associadas ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-125">The results are instances associated with the object.</span></span> <span data-ttu-id="b6e2d-126">Quando ASSOC é usado com um alias, as classes com a classe subjacente ao alias são retornadas.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="b6e2d-127">Por padrão, a saída é retornada no formato HTML.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="b6e2d-128">O verbo ASSOC tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="b6e2d-129">Opção</span><span class="sxs-lookup"><span data-stu-id="b6e2d-129">Switch</span></span>                         | <span data-ttu-id="b6e2d-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6e2d-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e2d-131">/RESULTCLASS:<classname></span><span class="sxs-lookup"><span data-stu-id="b6e2d-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="b6e2d-132">Os pontos de extremidade retornados associados ao objeto de origem devem pertencer ou derivar da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="b6e2d-133">/RESULTROLE:<rolename></span><span class="sxs-lookup"><span data-stu-id="b6e2d-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="b6e2d-134">Os pontos de extremidade retornados devem reproduzir uma função específica em associações com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="b6e2d-135">/ASSOCCLASS:<assocclass></span><span class="sxs-lookup"><span data-stu-id="b6e2d-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="b6e2d-136">Os pontos de extremidade retornados devem ser associados à origem por meio da classe especificada ou de uma de suas classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="b6e2d-137">Exemplo: **assoc. do sistema operacional**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-138"><span id="CALL"></span><span id="call"></span>LIGAÇÃO</span><span class="sxs-lookup"><span data-stu-id="b6e2d-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-139">Executa um método.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-139">Executes a method.</span></span>

<span data-ttu-id="b6e2d-140">Exemplo: **serviço em que Caption = ' telnet ' chama STARTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="b6e2d-141">Para determinar os métodos disponíveis para uma determinada classe, use **/?**.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="b6e2d-142">Por exemplo, **serviço em que Caption = "Telnet" Call/?**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="b6e2d-143">lista as funções disponíveis para a classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="b6e2d-144"><span id="CREATE"></span><span id="create"></span>CRIADA</span><span class="sxs-lookup"><span data-stu-id="b6e2d-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-145">Cria uma nova instância e define os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="b6e2d-146">CREATE não pode ser usado para criar uma nova classe.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="b6e2d-147">Exemplo: **ambiente Create Name = "Temp"; VARIABLEVALUE = "NEW"**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-148"><span id="DELETE"></span><span id="delete"></span>APAGAR</span><span class="sxs-lookup"><span data-stu-id="b6e2d-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-149">Exclui a instância atual ou o conjunto de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="b6e2d-150">DELETE pode ser usado para excluir uma classe.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="b6e2d-151">Exemplo: **processo em que Name = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-152"><span id="GET"></span><span id="get"></span>Obter</span><span class="sxs-lookup"><span data-stu-id="b6e2d-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-153">Recuperar valores de propriedade específicos.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-153">Retrieve specific property values.</span></span>

<span data-ttu-id="b6e2d-154">GET tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-154">GET has the following switches.</span></span>



| <span data-ttu-id="b6e2d-155">Opção</span><span class="sxs-lookup"><span data-stu-id="b6e2d-155">Switch</span></span>                               | <span data-ttu-id="b6e2d-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6e2d-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e2d-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-157">/VALUE</span></span>                               | <span data-ttu-id="b6e2d-158">A saída é formatada com cada valor listado em uma linha separada e com o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="b6e2d-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="b6e2d-159">/ALL</span></span>                                 | <span data-ttu-id="b6e2d-160">A saída é formatada como uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="b6e2d-161">Vertida<translation table></span><span class="sxs-lookup"><span data-stu-id="b6e2d-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="b6e2d-162">Traduza a saída usando a tabela de conversão chamada pelo comando.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="b6e2d-163">As tabelas de tradução BasicXml e novírgula estão incluídas com a WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="b6e2d-164">Cada<interval></span><span class="sxs-lookup"><span data-stu-id="b6e2d-164">/EVERY:<interval></span></span>              | <span data-ttu-id="b6e2d-165">Repita o comando a cada <interval> segundos.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="b6e2d-166">Ao<format specifier></span><span class="sxs-lookup"><span data-stu-id="b6e2d-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="b6e2d-167">Especifica um nome de arquivo de palavra-chave ou XSL para formatar os dados.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="b6e2d-168">Exemplo: **processar Get Name**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-169"><span id="LIST"></span><span id="list"></span>LISTA</span><span class="sxs-lookup"><span data-stu-id="b6e2d-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-170">Mostra os dados.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-170">Shows data.</span></span> <span data-ttu-id="b6e2d-171">LIST é o verbo padrão.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-171">LIST is the default verb.</span></span>

<span data-ttu-id="b6e2d-172">A lista tem os seguintes advérbios.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="b6e2d-173">Advérbio</span><span class="sxs-lookup"><span data-stu-id="b6e2d-173">Adverb</span></span>   | <span data-ttu-id="b6e2d-174">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6e2d-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="b6e2d-175">RESUMIDO</span><span class="sxs-lookup"><span data-stu-id="b6e2d-175">BRIEF</span></span>    | <span data-ttu-id="b6e2d-176">Conjunto principal das propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="b6e2d-177">FULL</span><span class="sxs-lookup"><span data-stu-id="b6e2d-177">FULL</span></span>     | <span data-ttu-id="b6e2d-178">Conjunto completo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-178">Full set of properties.</span></span> <span data-ttu-id="b6e2d-179">Esse é o advérbio padrão para a lista.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="b6e2d-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-180">INSTANCE</span></span> | <span data-ttu-id="b6e2d-181">Somente caminhos de instância.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="b6e2d-182">STATUS</span><span class="sxs-lookup"><span data-stu-id="b6e2d-182">STATUS</span></span>   | <span data-ttu-id="b6e2d-183">Status dos objetos.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="b6e2d-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="b6e2d-184">SYSTEM</span></span>   | <span data-ttu-id="b6e2d-185">Propriedades de sistema.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-185">System properties.</span></span>                                           |



 

<span data-ttu-id="b6e2d-186">A lista tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-186">LIST has the following switches.</span></span>



| <span data-ttu-id="b6e2d-187">Opção</span><span class="sxs-lookup"><span data-stu-id="b6e2d-187">Switch</span></span>                               | <span data-ttu-id="b6e2d-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6e2d-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e2d-189">Vertida<translation table></span><span class="sxs-lookup"><span data-stu-id="b6e2d-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="b6e2d-190">Traduza a saída usando a tabela de conversão chamada pelo comando.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="b6e2d-191">As tabelas de tradução BasicXml e novírgula estão incluídas com a WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="b6e2d-192">Cada<interval></span><span class="sxs-lookup"><span data-stu-id="b6e2d-192">/EVERY:<interval></span></span>              | <span data-ttu-id="b6e2d-193">Repita o comando a cada <interval> segundos.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="b6e2d-194">Ao<format specifier></span><span class="sxs-lookup"><span data-stu-id="b6e2d-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="b6e2d-195">Especifica um nome de arquivo de palavra-chave ou XSL para formatar os dados.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="b6e2d-196">Exemplo: **Resumo da lista de processos**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-197"><span id="SET"></span><span id="set"></span>Definição</span><span class="sxs-lookup"><span data-stu-id="b6e2d-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-198">Atribui valores a propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-198">Assigns values to properties.</span></span> <span data-ttu-id="b6e2d-199">Exemplo: **ambiente Set Name = "Temp"**, **VARIABLEVALUE = "New"**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="b6e2d-200">Comutadores</span><span class="sxs-lookup"><span data-stu-id="b6e2d-200">Switches</span></span>

<span data-ttu-id="b6e2d-201">Opções globais são usadas para definir padrões para o ambiente do WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="b6e2d-202">Você pode exibir o valor atual das condições definidas por essas opções inserindo o comando de **contexto** .</span><span class="sxs-lookup"><span data-stu-id="b6e2d-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="b6e2d-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-204">Namespace que o alias usa normalmente.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="b6e2d-205">O padrão é raiz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="b6e2d-206">Exemplo: **/namespace: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-208">O namespace WMIC normalmente procura aliases e outras informações de WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="b6e2d-209">Exemplo: **/Role: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-211">Nomes de computador, delimitado por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-211">Computer names, comma delimited.</span></span> <span data-ttu-id="b6e2d-212">Todos os comandos são executados de forma síncrona em todos os computadores listados nesse valor.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="b6e2d-213">Os nomes de arquivo devem ser prefixados com &.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-213">File names must be prefixed with &.</span></span> <span data-ttu-id="b6e2d-214">Os nomes de computador dentro de um arquivo devem ser delimitados por vírgula ou em linhas separadas.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="b6e2d-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-216">Nível de representação.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-216">Impersonation level.</span></span>

<span data-ttu-id="b6e2d-217">Exemplo: **/IMPLEVEL: Anonymous**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="b6e2d-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-219">Nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-219">Authentication level.</span></span>

<span data-ttu-id="b6e2d-220">Exemplo: **/AUTHLEVEL: PKT**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-222">Localidade.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-222">Locale.</span></span>

<span data-ttu-id="b6e2d-223">Exemplo: **/locale: MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="b6e2d-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-225">Habilitar ou desabilitar todos os privilégios.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="b6e2d-226">Exemplo: **/Privileges: Enable** ou **/Privileges: Disable**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-228">Exiba o êxito ou a falha de todas as funções usadas para executar comandos WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="b6e2d-229">Exemplo: **/trace: on** ou **/trace: off**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="b6e2d-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-231">Registra todas as saídas em um arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-231">Records all output to an XML file.</span></span> <span data-ttu-id="b6e2d-232">A saída também é exibida no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="b6e2d-233">Exemplo: **/Record:** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="b6e2d-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-235">Normalmente, os comandos DELETE são confirmados.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="b6e2d-236">Exemplo: **/Interactive: on** ou **/Interactive: off**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \| **off** \| *TimeoutInMilliseconds*</span><span class="sxs-lookup"><span data-stu-id="b6e2d-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-238">Se estiver executando ping nos computadores/NODE antes de enviar comandos WMIC para eles.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="b6e2d-239">Se um computador não responder, os comandos WMIC não serão enviados a ele.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="b6e2d-240">Exemplo: "/FAILFAST: ON" ou "/FAILFAST: OFF"</span><span class="sxs-lookup"><span data-stu-id="b6e2d-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="b6e2d-241">**/FAILFAST WMIC: 1000**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-242"><span id="_USER"></span><span id="_user"></span>/</span><span class="sxs-lookup"><span data-stu-id="b6e2d-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-243">Nome de usuário usado pela WMIC ao acessar os computadores ou computadores do/NODE especificados nos aliases.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="b6e2d-244">Você receberá uma solicitação de senha.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-244">You are prompted for the password.</span></span> <span data-ttu-id="b6e2d-245">Um nome de usuário não pode ser usado com o computador local.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="b6e2d-246">Exemplo: **/User:**_jsmith_</span><span class="sxs-lookup"><span data-stu-id="b6e2d-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="b6e2d-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-248">Senha usada pelo WMIC ao acessar os computadores/NODE.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-248">Password used by WMIC when accessing the /NODE computers.</span></span> <span data-ttu-id="b6e2d-249">A senha é visível na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-249">The password is visible at the command line.</span></span>

<span data-ttu-id="b6e2d-250">Exemplo: **/password:**_senha_</span><span class="sxs-lookup"><span data-stu-id="b6e2d-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6e2d-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-252">Especifica um modo para todo o redirecionamento de saída.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="b6e2d-253">A saída não aparece na linha de comando e o destino é limpo antes do início da saída.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="b6e2d-254">Os valores válidos são STDOUT, CLIPBOARD ou um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="b6e2d-255">Exemplo: **/output: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="b6e2d-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-257">Especifica um modo para todo o redirecionamento de saída.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="b6e2d-258">A saída não aparece na linha de comando e o destino não é limpo antes do início da saída e a saída é acrescentada ao final do conteúdo atual do destino.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="b6e2d-259">Os valores válidos são STDOUT, CLIPBOARD ou um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="b6e2d-260">Exemplo: **/Append: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="b6e2d-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-262">Usado com a **lista** e **obter** a opção/Every.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="b6e2d-263">Se a AGREGAção estiver ATIVAda, LISTe e obtenha a exibição dos resultados quando todos os computadores da/NODE tiverem respondido ou atingido o tempo limite. Se a AGREGAção estiver desativada, LISTe e exiba seus resultados assim que eles forem recebidos.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="b6e2d-264">Exemplo: **/Aggregate: off** ou **/Aggregate: on**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="b6e2d-265">Comandos</span><span class="sxs-lookup"><span data-stu-id="b6e2d-265">Commands</span></span>

<span data-ttu-id="b6e2d-266">Os comandos WMIC a seguir estão disponíveis o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="b6e2d-267">Para obter mais informações, consulte [comandos WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="b6e2d-268"><span id="CLASS"></span><span id="class"></span>CLASSES</span><span class="sxs-lookup"><span data-stu-id="b6e2d-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-269">Escape do modo de alias padrão do WMIC para acessar classes diretamente no esquema do WMI.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="b6e2d-270">Para obter mais informações sobre as classes WMI disponíveis, consulte [classes WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b6e2d-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="b6e2d-271">Exemplo: **WMIC/output: c: \\ClassOutput.htm classe Win32 \_ SoundDevice**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-272"><span id="PATH"></span><span id="path"></span>Multi-Path</span><span class="sxs-lookup"><span data-stu-id="b6e2d-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-273">Escape do modo de alias padrão do WMIC para acessar instâncias diretamente no esquema do WMI.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="b6e2d-274">Exemplo: **WMIC/output: c: \\PathOutput.txt caminho Win32 \_ SoundDevice get/value**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-275"><span id="CONTEXT"></span><span id="context"></span>NOTICIOSO</span><span class="sxs-lookup"><span data-stu-id="b6e2d-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-276">Exibe os valores atuais de todas as opções globais.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="b6e2d-277">Exemplo: **contexto WMIC**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-278"><span id="QUIT"></span><span id="quit"></span>Sai</span><span class="sxs-lookup"><span data-stu-id="b6e2d-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-279">Sair do WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-279">Exit from WMIC.</span></span>

<span data-ttu-id="b6e2d-280">Exemplo: **WMIC sair**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="b6e2d-281"><span id="EXIT"></span><span id="exit"></span>SIDO</span><span class="sxs-lookup"><span data-stu-id="b6e2d-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="b6e2d-282">Sair do WMIC.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-282">Exit from WMIC.</span></span>

<span data-ttu-id="b6e2d-283">Exemplo: **WMIC sair**</span><span class="sxs-lookup"><span data-stu-id="b6e2d-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b6e2d-284">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6e2d-284">Examples</span></span>

<span data-ttu-id="b6e2d-285">O [script para configurar a amostra de IP/sub-rede/gateway/DNS usando WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) na galeria do TechNet descreve como modificar e atualizar as configurações de IP, sub-rede, gateway e DNS.</span><span class="sxs-lookup"><span data-stu-id="b6e2d-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e2d-286">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e2d-286">Requirements</span></span>



| <span data-ttu-id="b6e2d-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e2d-287">Requirement</span></span> | <span data-ttu-id="b6e2d-288">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e2d-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b6e2d-289">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e2d-289">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e2d-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6e2d-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b6e2d-291">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e2d-291">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e2d-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6e2d-292">Windows Server 2008</span></span><br/> |



 

