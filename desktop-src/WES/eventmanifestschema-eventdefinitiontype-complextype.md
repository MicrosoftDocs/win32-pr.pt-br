---
title: Tipo complexo EventDefinitionType
description: Define um evento que seu provedor pode gravar.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Log de eventos do tipo complexo EventDefinitionType
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770541"
---
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="9f652-104">Tipo complexo EventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="9f652-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="9f652-105">Define um evento que seu provedor pode gravar.</span><span class="sxs-lookup"><span data-stu-id="9f652-105">Defines an event that your provider can write.</span></span>

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="9f652-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f652-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f652-107">Nome</span><span class="sxs-lookup"><span data-stu-id="9f652-107">Name</span></span></th>
<th><span data-ttu-id="9f652-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f652-108">Type</span></span></th>
<th><span data-ttu-id="9f652-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f652-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f652-110">channel</span><span class="sxs-lookup"><span data-stu-id="9f652-110">channel</span></span></td>
<td><span data-ttu-id="9f652-111">token</span><span class="sxs-lookup"><span data-stu-id="9f652-111">token</span></span></td>
<td><span data-ttu-id="9f652-112">Um identificador que identifica o canal no qual o evento é gravado.</span><span class="sxs-lookup"><span data-stu-id="9f652-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="9f652-113">Especifique um identificador de canal de um dos canais que você definiu ou importou.</span><span class="sxs-lookup"><span data-stu-id="9f652-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="9f652-114">Se o canal não especificar um identificador de canal, use o nome do canal.</span><span class="sxs-lookup"><span data-stu-id="9f652-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="9f652-115">Para obter detalhes sobre como definir ou importar um canal, consulte o tipo complexo <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="9f652-116">Se você não especificar um canal, o evento não será gravado em um canal.</span><span class="sxs-lookup"><span data-stu-id="9f652-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="9f652-117">Normalmente, o único motivo para não especificar um canal é se você estiver gravando eventos somente em uma sessão do ETW.</span><span class="sxs-lookup"><span data-stu-id="9f652-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="9f652-118">Para obter detalhes, consulte criando uma sessão do ETW, consulte <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controlando sessões de rastreamento de eventos</a>.</span><span class="sxs-lookup"><span data-stu-id="9f652-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f652-119">palavras-chave</span><span class="sxs-lookup"><span data-stu-id="9f652-119">keywords</span></span></td>
<td><span data-ttu-id="9f652-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNamelist</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f652-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="9f652-121">Uma lista separada por espaços de nomes de palavras-chave que identificam a categoria de eventos aos quais esse evento pertence.</span><span class="sxs-lookup"><span data-stu-id="9f652-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="9f652-122">Especifique um nome de palavra-chave na lista de palavras-chave que você definir.</span><span class="sxs-lookup"><span data-stu-id="9f652-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="9f652-123">Para obter detalhes sobre como definir palavras-chave, consulte o tipo complexo <a href="eventmanifestschema-keywordtype-complextype.md"><strong>keywordtype</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="9f652-124">Se você não especificar palavras-chave, o descritor de eventos conterá um zero para palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="9f652-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f652-125">nível</span><span class="sxs-lookup"><span data-stu-id="9f652-125">level</span></span></td>
<td><span data-ttu-id="9f652-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="9f652-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="9f652-127">O nível de detalhamento a ser usado ao gravar o evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="9f652-128">Especifique o nome de um nível que você definiu no manifesto ou um dos níveis definidos no arquivo de \Include\Winmeta.xml que está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9f652-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="9f652-129">Para obter detalhes sobre como definir um nível, consulte o tipo complexo <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="9f652-130">Se você não especificar um nível, o descritor de eventos conterá um zero para o nível.</span><span class="sxs-lookup"><span data-stu-id="9f652-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="9f652-131">Você deve especificar um nível se o tipo de canal para o qual o evento é gravado for admin; o nível deve ser um dos seguintes níveis definidos no Winmeata.xml:</span><span class="sxs-lookup"><span data-stu-id="9f652-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="9f652-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="9f652-132">win:Critical</span></span></li>
<li><span data-ttu-id="9f652-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="9f652-133">win:Error</span></span></li>
<li><span data-ttu-id="9f652-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="9f652-134">win:Warning</span></span></li>
<li><span data-ttu-id="9f652-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="9f652-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f652-136">message</span><span class="sxs-lookup"><span data-stu-id="9f652-136">message</span></span></td>
<td><span data-ttu-id="9f652-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f652-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="9f652-138">A mensagem localizada para o evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-138">The localized message for the event.</span></span> <span data-ttu-id="9f652-139">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> do manifesto.</span><span class="sxs-lookup"><span data-stu-id="9f652-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="9f652-140">Você deverá especificar uma mensagem se o tipo de canal para o qual o evento é gravado for admin.</span><span class="sxs-lookup"><span data-stu-id="9f652-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f652-141">Não registrado em log</span><span class="sxs-lookup"><span data-stu-id="9f652-141">notLogged</span></span></td>
<td><span data-ttu-id="9f652-142">booleano</span><span class="sxs-lookup"><span data-stu-id="9f652-142">boolean</span></span></td>
<td><span data-ttu-id="9f652-143">Determina se o provedor registra esse evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="9f652-144">Especifique true se o provedor registrar esse evento; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="9f652-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="9f652-145">Use esse atributo para indicar que o provedor não está mais registrando esse evento em vez de remover o evento do manifesto.</span><span class="sxs-lookup"><span data-stu-id="9f652-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="9f652-146">Manter o evento no manifesto permitirá que os consumidores decodifiquem arquivos ETL mais antigos que incluam o evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="9f652-147"><strong>Windows Server 2008 e Windows Vista:</strong> Não há suporte para esse atributo em versões do compilador de mensagens enviadas antes da versão do Windows 7 do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="9f652-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f652-148">opcode</span><span class="sxs-lookup"><span data-stu-id="9f652-148">opcode</span></span></td>
<td><span data-ttu-id="9f652-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="9f652-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="9f652-150">O nome de um opcode que identifica uma operação dentro da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9f652-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="9f652-151">Especifique o nome de um opcode que você definiu no manifesto ou um dos opcodes definidos em Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="9f652-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="9f652-152">Para obter detalhes sobre como definir um opcode, consulte o tipo complexo <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpCodeType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="9f652-153">Se a tarefa que você referencia contém opcodes específicos da tarefa (local), você pode especificar um de seus opcodes específicos da tarefa ou um opcode definido no nível do provedor (um opcode global).</span><span class="sxs-lookup"><span data-stu-id="9f652-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="9f652-154">Se você especificar um opcode global, o valor do opcode global não poderá ser o mesmo que um dos opcodes locais para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="9f652-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="9f652-155">Se você fizer referência a um opcode local, o atributo Task deverá fazer referência à tarefa à qual o opcode local pertence.</span><span class="sxs-lookup"><span data-stu-id="9f652-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="9f652-156">Se você não especificar um opcode, o descritor de eventos conterá um zero para opcode.</span><span class="sxs-lookup"><span data-stu-id="9f652-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f652-157">símbolo</span><span class="sxs-lookup"><span data-stu-id="9f652-157">symbol</span></span></td>
<td><span data-ttu-id="9f652-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f652-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="9f652-159">O símbolo a ser usado para referenciar o descritor de eventos para esse evento em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f652-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="9f652-160">O <a href="message-compiler--mc-exe-.md"><strong>compilador de mensagens (MC.exe)</strong></a> usa o símbolo para criar uma constante para o descritor de eventos no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="9f652-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="9f652-161">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="9f652-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="9f652-162">Você usa o descritor ao chamar a função <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> para gravar o evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f652-163">task</span><span class="sxs-lookup"><span data-stu-id="9f652-163">task</span></span></td>
<td><span data-ttu-id="9f652-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="9f652-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="9f652-165">O nome de uma tarefa que identifica o componente ou subcomponente que gera esse evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="9f652-166">Especifique o nome de uma tarefa que você definiu no manifesto.</span><span class="sxs-lookup"><span data-stu-id="9f652-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="9f652-167">Para obter detalhes sobre como definir uma tarefa, consulte o tipo complexo <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="9f652-168">Se você não especificar uma tarefa, o descritor de eventos conterá um zero para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="9f652-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f652-169">template</span><span class="sxs-lookup"><span data-stu-id="9f652-169">template</span></span></td>
<td><span data-ttu-id="9f652-170">token</span><span class="sxs-lookup"><span data-stu-id="9f652-170">token</span></span></td>
<td><span data-ttu-id="9f652-171">O identificador de modelo do modelo que define os itens de dados que esse evento inclui.</span><span class="sxs-lookup"><span data-stu-id="9f652-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="9f652-172">Especifique o identificador de um modelo que você definiu no manifesto.</span><span class="sxs-lookup"><span data-stu-id="9f652-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="9f652-173">Para obter detalhes sobre como definir um modelo, consulte o tipo complexo <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9f652-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f652-174">value</span><span class="sxs-lookup"><span data-stu-id="9f652-174">value</span></span></td>
<td><span data-ttu-id="9f652-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f652-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="9f652-176">O identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-176">The event identifier.</span></span> <span data-ttu-id="9f652-177">O identificador deve ser exclusivo na lista de eventos que você definir.</span><span class="sxs-lookup"><span data-stu-id="9f652-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f652-178">version</span><span class="sxs-lookup"><span data-stu-id="9f652-178">version</span></span></td>
<td><span data-ttu-id="9f652-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="9f652-179">unsignedByte</span></span></td>
<td><span data-ttu-id="9f652-180">Um número de versão de um byte da definição de evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9f652-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f652-181">Remarks</span></span>

<span data-ttu-id="9f652-182">Se você usar [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) para formatar a cadeia de caracteres da mensagem para o evento (ou usar o Visualizador de eventos para exibir a cadeia de caracteres da mensagem), a cadeia de caracteres de mensagem poderá conter cadeias de inserção e qualquer uma das cadeias de caracteres de formato suportadas pela função **FormatMessage** do Win32.</span><span class="sxs-lookup"><span data-stu-id="9f652-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="9f652-183">As cadeias de caracteres de inserção estão limitadas a%*n* ou%*n*! s!</span><span class="sxs-lookup"><span data-stu-id="9f652-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="9f652-184">(por exemplo, %1) em que *n* é a referência baseada em um dos itens de dados definidos no modelo do evento.</span><span class="sxs-lookup"><span data-stu-id="9f652-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="9f652-185">A cadeia de caracteres de mensagem também pode conter cadeias de inserção de parâmetro no formato%%*n* (por exemplo,% %4).</span><span class="sxs-lookup"><span data-stu-id="9f652-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="9f652-186">O número máximo de cadeias de caracteres de inserção que a mensagem pode conter é 100.</span><span class="sxs-lookup"><span data-stu-id="9f652-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f652-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f652-187">Requirements</span></span>



| <span data-ttu-id="9f652-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f652-188">Requirement</span></span> | <span data-ttu-id="9f652-189">Valor</span><span class="sxs-lookup"><span data-stu-id="9f652-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f652-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f652-190">Minimum supported client</span></span><br/> | <span data-ttu-id="9f652-191">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f652-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f652-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f652-192">Minimum supported server</span></span><br/> | <span data-ttu-id="9f652-193">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f652-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

