---
title: Definindo modelos de dados de evento
description: Os provedores usam modelos de dados para definir os dados específicos de eventos que eles incluem com um evento e para definir os dados de filtro que uma sessão de rastreamento ETW pode passar para o provedor quando ele habilita o provedor.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103823608"
---
# <a name="defining-event-data-templates"></a><span data-ttu-id="7a62e-103">Definindo modelos de dados de evento</span><span class="sxs-lookup"><span data-stu-id="7a62e-103">Defining Event Data Templates</span></span>

<span data-ttu-id="7a62e-104">Os provedores usam modelos de dados para definir os dados específicos de eventos que eles incluem com um evento e para definir os dados de filtro que uma sessão de rastreamento ETW pode passar para o provedor quando ele habilita o provedor.</span><span class="sxs-lookup"><span data-stu-id="7a62e-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="7a62e-105">Se o evento não incluir dados específicos do evento, você não definirá um modelo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="7a62e-106">Para definir um modelo, use o elemento **Template** .</span><span class="sxs-lookup"><span data-stu-id="7a62e-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="7a62e-107">Um modelo inclui um item de dados para cada parte dos dados que o provedor inclui com o evento.</span><span class="sxs-lookup"><span data-stu-id="7a62e-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="7a62e-108">Você pode especificar tipos, cadeias de caracteres, matrizes e estruturas integrais.</span><span class="sxs-lookup"><span data-stu-id="7a62e-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="7a62e-109">Você deve gravar os dados do evento na ordem em que os itens de dados foram definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="7a62e-110">Você também pode incluir no modelo um fragmento XML que os consumidores devem usar para determinar como renderizar os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="7a62e-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="7a62e-111">Se você não incluir o fragmento, os consumidores deverão renderizar os dados do evento na ordem em que os itens de dados foram definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="7a62e-112">Ao definir um modelo, você deve dar a ele um identificador de modelo que você usa para fazer referência ao modelo em uma definição de evento.</span><span class="sxs-lookup"><span data-stu-id="7a62e-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="7a62e-113">Cada item de dados no modelo deve especificar um nome e um tipo de dados de entrada (para obter uma lista de tipos de entrada, consulte a seção comentários do tipo complexo [**InputType**](eventmanifestschema-inputtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="7a62e-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="7a62e-114">Se o tipo de dados de entrada puder ser renderizado em vários formatos, você deverá especificar o tipo de dados de saída que informa aos consumidores como renderizar o item de dados.</span><span class="sxs-lookup"><span data-stu-id="7a62e-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="7a62e-115">Por exemplo, um tipo de dados de entrada UInt32 pode ser renderizado como um inteiro não assinado, um identificador de thread, um endereço IPv4 e um código de erro Win32 entre outros.</span><span class="sxs-lookup"><span data-stu-id="7a62e-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="7a62e-116">Se você não especificar o tipo de dados de saída, os consumidores deverão usar o tipo de saída padrão do tipo de entrada para renderizar o item de dados.</span><span class="sxs-lookup"><span data-stu-id="7a62e-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="7a62e-117">Para especificar uma matriz, inclua o atributo **Count** no item de dados e defina-o como o número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="7a62e-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="7a62e-118">A matriz pode ser uma matriz de tamanho variável ou uma matriz de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="7a62e-119">Se a matriz for uma matriz de tamanho fixo, defina **Count** como o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="7a62e-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="7a62e-120">Por exemplo, se uma matriz de inteiros tiver um tamanho fixo de 10, defina a **contagem** como 10.</span><span class="sxs-lookup"><span data-stu-id="7a62e-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="7a62e-121">Ao gravar a matriz, você deve gravar 40 bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="7a62e-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="7a62e-122">Se a matriz for uma matriz de tamanho variável, defina **Count** como o nome do item de dados que contém o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="7a62e-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="7a62e-123">Se a matriz contiver ponteiros, o endereço dos ponteiros será gravado como os dados do evento, não os dados aos quais os ponteiros apontam.</span><span class="sxs-lookup"><span data-stu-id="7a62e-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="7a62e-124">Você deve especificar o atributo **Length** se o item de dados for um blob binário.</span><span class="sxs-lookup"><span data-stu-id="7a62e-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="7a62e-125">Você também pode especificar o atributo **Length** para cadeias de caracteres de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="7a62e-126">Especifique o atributo de **mapa** se o item de dados representar um valor de enumeração e você quiser que o consumidor imprima uma cadeia de caracteres para o valor em vez do próprio valor.</span><span class="sxs-lookup"><span data-stu-id="7a62e-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="7a62e-127">Se você incluir estruturas no modelo, deverá escrever os membros da estrutura individualmente em vez de escrever a estrutura, a menos que possa garantir o alinhamento de limites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="7a62e-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="7a62e-128">Você deve considerar cuidadosamente as informações que você inclui nos eventos, especialmente quando os eventos são gravados nos canais globais.</span><span class="sxs-lookup"><span data-stu-id="7a62e-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="7a62e-129">Como regra geral, você não deve incluir informações particulares nos eventos.</span><span class="sxs-lookup"><span data-stu-id="7a62e-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="7a62e-130">Isso inclui senhas de texto sem formatação e informações de usuário pessoal.</span><span class="sxs-lookup"><span data-stu-id="7a62e-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="7a62e-131">Além disso, os programas executados pelo usuário, URLs que o usuário visitou e outras informações relacionadas às atividades do usuário no computador devem ser consideradas particulares.</span><span class="sxs-lookup"><span data-stu-id="7a62e-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="7a62e-132">Se você precisar registrar URLs e nomes de usuário nos eventos, não os grave nos canais do Windows (sistema e aplicativo), pois esses canais podem ser lidos por todos os usuários autenticados.</span><span class="sxs-lookup"><span data-stu-id="7a62e-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="7a62e-133">Em vez disso, grave-os em seus próprios canais operacionais ou analíticos.</span><span class="sxs-lookup"><span data-stu-id="7a62e-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="7a62e-134">Defina as permissões de acesso nesses canais para permitir que somente os administradores leiam os eventos.</span><span class="sxs-lookup"><span data-stu-id="7a62e-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="7a62e-135">Talvez seja necessário fornecer uma divulgação apropriada para notificar os usuários do fato de que as informações privadas são disponibilizadas para os administradores.</span><span class="sxs-lookup"><span data-stu-id="7a62e-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="7a62e-136">O exemplo a seguir mostra como definir um modelo.</span><span class="sxs-lookup"><span data-stu-id="7a62e-136">The following example shows how to define a template.</span></span> <span data-ttu-id="7a62e-137">Você deve especificar o atributo **tid** do modelo referenciado na definição de evento ou definição de filtro.</span><span class="sxs-lookup"><span data-stu-id="7a62e-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
