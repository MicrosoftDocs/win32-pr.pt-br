---
title: Tipo complexo de TaskType
description: Define um componente ou subcomponente de um aplicativo. | Tipo complexo de TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType tipo complexo de log de eventos
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763752"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="b6c16-105">Tipo complexo de TaskType</span><span class="sxs-lookup"><span data-stu-id="b6c16-105">TaskType Complex Type</span></span>

<span data-ttu-id="b6c16-106">Define um componente ou subcomponente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6c16-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b6c16-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b6c16-107">Child elements</span></span>



| <span data-ttu-id="b6c16-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6c16-108">Element</span></span>                                                         | <span data-ttu-id="b6c16-109">Type</span><span class="sxs-lookup"><span data-stu-id="b6c16-109">Type</span></span>                                                                     | <span data-ttu-id="b6c16-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6c16-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6c16-111">**opcodes**</span><span class="sxs-lookup"><span data-stu-id="b6c16-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="b6c16-112">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="b6c16-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="b6c16-113">Define uma lista de opcodes específicos da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="b6c16-114">Você não pode usar os valores de opcode definidos em Winmeta.xml para opcodes específicos da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b6c16-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6c16-115">Attributes</span></span>



| <span data-ttu-id="b6c16-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b6c16-116">Name</span></span>      | <span data-ttu-id="b6c16-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6c16-117">Type</span></span>                                                              | <span data-ttu-id="b6c16-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6c16-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c16-119">eventGUID</span><span class="sxs-lookup"><span data-stu-id="b6c16-119">eventGUID</span></span> | [<span data-ttu-id="b6c16-120">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="b6c16-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="b6c16-121">Um identificador global exclusivo, no formato de registro, que identifica a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="b6c16-122">Esse atributo é necessário se você usar o argumento-MOF de mensagens do compilador para gerar uma classe MOF para suporte de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="b6c16-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="b6c16-123">message</span><span class="sxs-lookup"><span data-stu-id="b6c16-123">message</span></span>   | [<span data-ttu-id="b6c16-124">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="b6c16-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b6c16-125">O nome de exibição localizado para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-125">The localized display name for the task.</span></span> <span data-ttu-id="b6c16-126">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="b6c16-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="b6c16-127">name</span><span class="sxs-lookup"><span data-stu-id="b6c16-127">name</span></span>      | <span data-ttu-id="b6c16-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="b6c16-128">**QName**</span></span>                                                         | <span data-ttu-id="b6c16-129">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b6c16-130">símbolo</span><span class="sxs-lookup"><span data-stu-id="b6c16-130">symbol</span></span>    | [<span data-ttu-id="b6c16-131">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="b6c16-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b6c16-132">O símbolo a ser usado para fazer referência à tarefa em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6c16-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="b6c16-133">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para a tarefa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="b6c16-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="b6c16-134">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="b6c16-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="b6c16-135">value</span><span class="sxs-lookup"><span data-stu-id="b6c16-135">value</span></span>     | [<span data-ttu-id="b6c16-136">**UInt16type**</span><span class="sxs-lookup"><span data-stu-id="b6c16-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="b6c16-137">Um valor numérico que identifica exclusivamente essa tarefa na lista de tarefas que o provedor define.</span><span class="sxs-lookup"><span data-stu-id="b6c16-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="b6c16-138">O valor deve estar no intervalo de 1 a 239.</span><span class="sxs-lookup"><span data-stu-id="b6c16-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="b6c16-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6c16-139">Examples</span></span>

<span data-ttu-id="b6c16-140">O exemplo a seguir mostra como especificar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="b6c16-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="b6c16-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c16-141">Requirements</span></span>



| <span data-ttu-id="b6c16-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c16-142">Requirement</span></span> | <span data-ttu-id="b6c16-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c16-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6c16-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c16-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c16-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6c16-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6c16-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c16-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c16-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6c16-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





