---
description: Os provedores clássicos devem usar formato MOF (MOF) para publicar o layout de seus dados de evento. Os consumidores podem ler o layout publicado do WMI em tempo de execução e usá-lo para ler os dados do evento.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publicando seu esquema de evento para um provedor clássico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296425"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="51deb-104">Publicando seu esquema de evento para um provedor clássico</span><span class="sxs-lookup"><span data-stu-id="51deb-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="51deb-105">Os provedores [clássicos](about-event-tracing.md) devem usar [formato MOF](../wmisdk/managed-object-format--mof-.md) (MOF) para publicar o layout de seus dados de evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="51deb-106">Os consumidores podem ler o layout publicado do WMI em tempo de execução e usá-lo para ler os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="51deb-107">Se você usar o MOF para publicar o layout dos dados de evento no WMI, normalmente criará os três tipos de classes MOF a seguir no \\ namespace WMI raiz:</span><span class="sxs-lookup"><span data-stu-id="51deb-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="51deb-108">Uma classe MOF de provedor</span><span class="sxs-lookup"><span data-stu-id="51deb-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="51deb-109">Uma ou mais classes MOF de evento</span><span class="sxs-lookup"><span data-stu-id="51deb-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="51deb-110">Uma ou mais classes MOF de tipo de evento</span><span class="sxs-lookup"><span data-stu-id="51deb-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="51deb-111">Classes MOF do provedor</span><span class="sxs-lookup"><span data-stu-id="51deb-111">Provider MOF classes</span></span>

<span data-ttu-id="51deb-112">Se você publicar o layout dos dados do evento, deverá criar uma classe MOF que identifique seu provedor.</span><span class="sxs-lookup"><span data-stu-id="51deb-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="51deb-113">Essa classe deve derivar da classe **EventTrace** MOF e deve estar vazia (sem propriedades ou métodos).</span><span class="sxs-lookup"><span data-stu-id="51deb-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="51deb-114">A classe também deve incluir o qualificador **GUID** que identifica exclusivamente o provedor.</span><span class="sxs-lookup"><span data-stu-id="51deb-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="51deb-115">Esse é o mesmo GUID que você usa ao chamar a função [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) para registrar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="51deb-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="51deb-116">Classes do evento MOF</span><span class="sxs-lookup"><span data-stu-id="51deb-116">Event MOF classes</span></span>

<span data-ttu-id="51deb-117">Uma classe MOF de evento define uma classe de eventos que o provedor fornece.</span><span class="sxs-lookup"><span data-stu-id="51deb-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="51deb-118">Essa classe deriva da classe MOF do provedor e deve estar vazia (sem propriedades ou métodos).</span><span class="sxs-lookup"><span data-stu-id="51deb-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="51deb-119">A classe também deve incluir o qualificador **GUID** que identifica exclusivamente a classe de eventos que suas classes filhas definem.</span><span class="sxs-lookup"><span data-stu-id="51deb-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="51deb-120">O provedor usa esse mesmo GUID ao definir o membro **GUID** da estrutura [**do \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="51deb-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="51deb-121">Classes MOF de tipo de evento</span><span class="sxs-lookup"><span data-stu-id="51deb-121">Event type MOF classes</span></span>

<span data-ttu-id="51deb-122">Uma classe de tipo de evento MOF define os dados de evento reais.</span><span class="sxs-lookup"><span data-stu-id="51deb-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="51deb-123">Essa classe deriva de sua classe MOF de evento pai.</span><span class="sxs-lookup"><span data-stu-id="51deb-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="51deb-124">Ao nomear a classe MOF do tipo de evento, a Convenção é usar o nome da classe MOF do evento no início do tipo de evento nome da classe MOF.</span><span class="sxs-lookup"><span data-stu-id="51deb-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="51deb-125">Por exemplo, se o nome da classe MOF do evento for HWConfig e a classe MOF de tipo de evento representar informações de CPU, você deverá nomear o tipo de evento classe MOF, \_ CPU HWConfig.</span><span class="sxs-lookup"><span data-stu-id="51deb-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="51deb-126">Use o qualificador **EventType** na classe do tipo de evento MOF para identificar o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="51deb-127">Se vários tipos de eventos usarem os mesmos dados de evento, eles poderão usar a mesma classe MOF.</span><span class="sxs-lookup"><span data-stu-id="51deb-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="51deb-128">O provedor usa o mesmo valor de tipo de evento para identificar o evento ao definir o membro **Class. Type** da estrutura do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="51deb-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="51deb-129">A classe MOF de tipo de evento contém propriedades.</span><span class="sxs-lookup"><span data-stu-id="51deb-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="51deb-130">A ordem dessas propriedades define o layout dos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="51deb-131">A tabela a seguir identifica os tipos de dados e qualificadores que você pode usar para definir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="51deb-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="51deb-132">Para obter mais informações sobre os qualificadores de classe e propriedade que você pode usar, consulte [qualificadores MOF de rastreamento de eventos](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="51deb-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="51deb-133">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="51deb-133">Data type</span></span>              | <span data-ttu-id="51deb-134">Qualificadores</span><span class="sxs-lookup"><span data-stu-id="51deb-134">Qualifiers</span></span>                        | <span data-ttu-id="51deb-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="51deb-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51deb-136">**sint8**, **uint8**</span><span class="sxs-lookup"><span data-stu-id="51deb-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="51deb-137">**Formato**</span><span class="sxs-lookup"><span data-stu-id="51deb-137">**Format**</span></span>                        | <span data-ttu-id="51deb-138">Declara um inteiro decimal de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="51deb-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="51deb-139">Para declarar um caractere ANSI, use o qualificador de **formato** e defina seu valor como "c".</span><span class="sxs-lookup"><span data-stu-id="51deb-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="51deb-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51deb-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="51deb-141">**Formato**</span><span class="sxs-lookup"><span data-stu-id="51deb-141">**Format**</span></span>                        | <span data-ttu-id="51deb-142">Declara um inteiro decimal de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="51deb-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="51deb-143">Para indicar que o número é um número hexadecimal, use o qualificador de **formato** .</span><span class="sxs-lookup"><span data-stu-id="51deb-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="51deb-144">Por exemplo, Format ("x").</span><span class="sxs-lookup"><span data-stu-id="51deb-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="51deb-145">**sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51deb-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="51deb-146">**Formato**</span><span class="sxs-lookup"><span data-stu-id="51deb-146">**Format**</span></span>                        | <span data-ttu-id="51deb-147">Declara um inteiro decimal de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="51deb-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="51deb-148">Para indicar que o número é um número hexadecimal, use o qualificador de **formato** e defina seu valor como "x".</span><span class="sxs-lookup"><span data-stu-id="51deb-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="51deb-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="51deb-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="51deb-150">**Formato**</span><span class="sxs-lookup"><span data-stu-id="51deb-150">**Format**</span></span>                        | <span data-ttu-id="51deb-151">Declara um inteiro decimal de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="51deb-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="51deb-152">Para indicar que o número é um número hexadecimal, use o qualificador de **formato** e defina seu valor como "x".</span><span class="sxs-lookup"><span data-stu-id="51deb-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="51deb-153">**booleano**</span><span class="sxs-lookup"><span data-stu-id="51deb-153">**boolean**</span></span>            |                                   | <span data-ttu-id="51deb-154">Declara um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="51deb-154">Declares a Boolean value.</span></span> <span data-ttu-id="51deb-155">O consumidor do evento deve interpretar o valor como BOOL (inteiro de 4 bytes).</span><span class="sxs-lookup"><span data-stu-id="51deb-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="51deb-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="51deb-156">**char16**</span></span>             |                                   | <span data-ttu-id="51deb-157">Declara um caractere largo.</span><span class="sxs-lookup"><span data-stu-id="51deb-157">Declares a wide character.</span></span> <span data-ttu-id="51deb-158">O consumidor de evento deve interpretar matrizes char16 em eventos de kernel como cadeias de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="51deb-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="51deb-159">(Use o tamanho da matriz para copiar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51deb-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="51deb-160">Algumas cadeias de caracteres podem conter espaços nulos à esquerda.)</span><span class="sxs-lookup"><span data-stu-id="51deb-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="51deb-161">**object**</span><span class="sxs-lookup"><span data-stu-id="51deb-161">**object**</span></span>             | <span data-ttu-id="51deb-162">**Extensão**</span><span class="sxs-lookup"><span data-stu-id="51deb-162">**Extension**</span></span>                     | <span data-ttu-id="51deb-163">Declara um blob binário.</span><span class="sxs-lookup"><span data-stu-id="51deb-163">Declares a binary blob.</span></span> <span data-ttu-id="51deb-164">O qualificador de **extensão** indica o tipo de dados no BLOB.</span><span class="sxs-lookup"><span data-stu-id="51deb-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="51deb-165">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="51deb-165">**string**</span></span>             | <span data-ttu-id="51deb-166">**Formato**, **StringTermination**</span><span class="sxs-lookup"><span data-stu-id="51deb-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="51deb-167">Declara um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="51deb-167">Declares a string value.</span></span> <span data-ttu-id="51deb-168">Para indicar que a cadeia de caracteres é uma cadeia de caracteres largos, use o qualificador de **formato** e defina seu valor como "w".</span><span class="sxs-lookup"><span data-stu-id="51deb-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="51deb-169">A cadeia de caracteres será considerada uma cadeia de caracteres ANSI se você não especificar o qualificador de **formato** .</span><span class="sxs-lookup"><span data-stu-id="51deb-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="51deb-170">Para indicar como a cadeia de caracteres é encerrada, use o qualificador **StringTermination** .</span><span class="sxs-lookup"><span data-stu-id="51deb-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="51deb-171">Para especificar uma matriz, você pode usar colchetes, \[ \] .</span><span class="sxs-lookup"><span data-stu-id="51deb-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="51deb-172">Os colchetes podem incluir o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="51deb-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="51deb-173">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51deb-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="51deb-174">Você também pode usar o qualificador **máximo** para especificar o tamanho de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="51deb-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="51deb-175">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51deb-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="51deb-176">Se você incluir o tamanho da matriz entre colchetes, o compilador MOF gerará o qualificador máximo para você.</span><span class="sxs-lookup"><span data-stu-id="51deb-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="51deb-177">É importante que você use o qualificador de **Descrição** para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="51deb-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="51deb-178">A descrição deve conter um nome de exibição que o consumidor possa usar ao exibir os valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="51deb-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="51deb-179">O exemplo a seguir mostra o conteúdo de um arquivo MOF que descreve um provedor, evento e classe de tipo de evento MOF.</span><span class="sxs-lookup"><span data-stu-id="51deb-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="51deb-180">Observe que os nomes de classe MOF do provedor, do evento e do tipo de evento devem ser exclusivos em todo o namespace.</span><span class="sxs-lookup"><span data-stu-id="51deb-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="51deb-181">Para evitar conflitos de nomenclatura, você deve usar um nome exclusivo e descritivo para todos os nomes de classe.</span><span class="sxs-lookup"><span data-stu-id="51deb-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="51deb-182">As propriedades de classe também devem ser descritivas e exclusivas em sua hierarquia de classe — uma classe filha que contém o mesmo nome de propriedade que uma classe pai substitui a propriedade da classe pai.</span><span class="sxs-lookup"><span data-stu-id="51deb-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="51deb-183">Depois de definir suas classes MOF, use o compilador MOF para gerar seu esquema de evento e adicioná-lo ao repositório CIM.</span><span class="sxs-lookup"><span data-stu-id="51deb-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="51deb-184">Os consumidores podem ler o esquema do repositório e ler programaticamente os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="51deb-185">Para obter uma descrição completa da sintaxe do MOF e usar o compilador MOF (Mofcomp.exe) para adicionar suas classes MOF ao repositório CIM, consulte [formato MOF](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="51deb-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="51deb-186">Para obter informações sobre como usar Wbemtest.exe para acessar o repositório CIM, consulte [Instrumentação de gerenciamento do Windows](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="51deb-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="51deb-187">Classe MOF de controle de versão</span><span class="sxs-lookup"><span data-stu-id="51deb-187">Versioning MOF class</span></span>

<span data-ttu-id="51deb-188">Se você adicionar ou alterar uma classe MOF de tipo de evento, a Convenção será a versão da classe MOF de evento e de seu tipo de evento filho classes MOF.</span><span class="sxs-lookup"><span data-stu-id="51deb-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="51deb-189">Para obter a versão da classe MOF do evento atual, acrescente \_ vn ao nome da classe, em que n é um número incremental começando em 0.</span><span class="sxs-lookup"><span data-stu-id="51deb-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="51deb-190">Se esta for a primeira revisão para a classe, acrescente \_ V0 ao nome da classe.</span><span class="sxs-lookup"><span data-stu-id="51deb-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="51deb-191">Você também deve adicionar o qualificador **EventVersion** à classe.</span><span class="sxs-lookup"><span data-stu-id="51deb-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="51deb-192">Use o mesmo número de versão usado no nome de classe para o valor do qualificador **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="51deb-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="51deb-193">A nova versão da classe MOF de evento deve usar o mesmo nome e qualificador **GUID** da classe original.</span><span class="sxs-lookup"><span data-stu-id="51deb-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="51deb-194">A nova classe pode opcionalmente adicionar o qualificador **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="51deb-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="51deb-195">A classe MOF de evento que não contém o qualificador **EventVersion** é considerada a versão mais recente, ou se todas as versões da classe contiverem um qualificador **EventVersion** , a classe com o número de versão mais alto será considerada a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="51deb-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="51deb-196">O provedor usa o membro **Class. Version** da estrutura [**de \_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar a versão do evento incluído no rastreamento.</span><span class="sxs-lookup"><span data-stu-id="51deb-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="51deb-197">O exemplo a seguir mostra como fazer a versão de uma classe MOF de evento.</span><span class="sxs-lookup"><span data-stu-id="51deb-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
