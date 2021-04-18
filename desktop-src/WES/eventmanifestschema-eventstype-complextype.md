---
title: Tipo complexo EventType
description: Contém uma lista de provedores que são definidos no manifesto. | Tipo complexo EventType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventLog tipo complexo de EventType
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788821"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="e593f-105">Tipo complexo EventType</span><span class="sxs-lookup"><span data-stu-id="e593f-105">EventsType Complex Type</span></span>

<span data-ttu-id="e593f-106">Contém uma lista de provedores que são definidos no manifesto.</span><span class="sxs-lookup"><span data-stu-id="e593f-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e593f-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e593f-107">Child elements</span></span>

| <span data-ttu-id="e593f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e593f-108">Element</span></span> | <span data-ttu-id="e593f-109">Type</span><span class="sxs-lookup"><span data-stu-id="e593f-109">Type</span></span> | <span data-ttu-id="e593f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e593f-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="e593f-111">message</span><span class="sxs-lookup"><span data-stu-id="e593f-111">message</span></span> |      | <span data-ttu-id="e593f-112">Define uma cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-112">Defines a message string.</span></span> |
| <span data-ttu-id="e593f-113">mensagem de</span><span class="sxs-lookup"><span data-stu-id="e593f-113">messageTable</span></span> | | <span data-ttu-id="e593f-114">Define uma lista de cadeias de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-114">Defines a list of message strings.</span></span> <span data-ttu-id="e593f-115">Você não deve ter que usar uma tabela de mensagens, exceto nos casos a seguir, em que você deve definir uma tabela de mensagens para atribuir explicitamente números de recursos a cadeias de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="e593f-116">Você está migrando de um arquivo de texto de mensagem (. MC) para um manifesto, mas ainda está gravando eventos para os canais do aplicativo e do sistema, para que os consumidores herdados continuem consumindo os eventos.</span><span class="sxs-lookup"><span data-stu-id="e593f-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="e593f-117">Para fazer isso funcionar, os identificadores de recurso para as cadeias de caracteres de mensagem definidos no manifesto devem ser iguais aos identificadores de evento.</span><span class="sxs-lookup"><span data-stu-id="e593f-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="e593f-118">No entanto, o compilador de mensagem atribui automaticamente identificadores de recurso às cadeias de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="e593f-119">Para substituir o compilador, use a tabela Message e defina o atributo Value para o identificador de evento e o atributo Message para se referir a uma cadeia de caracteres na tabela de cadeia de caracteres na seção localização do manifesto.</span><span class="sxs-lookup"><span data-stu-id="e593f-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="e593f-120">Se você quiser identificar mais de 16 provedores, deverá incluir a tabela de mensagens que os provedores seventeenth e on devem usar para atribuir valores de recursos para as cadeias de caracteres de mensagem que eles definem.</span><span class="sxs-lookup"><span data-stu-id="e593f-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="e593f-121">Se o provedor fizer referência a cadeias de caracteres de mensagem que os provedores de 1 a 16 definidos, você não incluirá essas cadeias de caracteres de mensagem na tabela de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e593f-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="e593f-122">**operador**</span><span class="sxs-lookup"><span data-stu-id="e593f-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="e593f-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="e593f-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="e593f-124">Uma lista de provedores que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="e593f-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="e593f-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="e593f-125">Attributes</span></span>

| <span data-ttu-id="e593f-126">Nome</span><span class="sxs-lookup"><span data-stu-id="e593f-126">Name</span></span>    | <span data-ttu-id="e593f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e593f-127">Type</span></span>                                                             | <span data-ttu-id="e593f-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e593f-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e593f-129">message</span><span class="sxs-lookup"><span data-stu-id="e593f-129">message</span></span> | [<span data-ttu-id="e593f-130">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="e593f-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="e593f-131">Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e593f-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="e593f-132">mid</span><span class="sxs-lookup"><span data-stu-id="e593f-132">mid</span></span>     | <span data-ttu-id="e593f-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="e593f-133">xs:string</span></span>                                                        | <span data-ttu-id="e593f-134">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e593f-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="e593f-135">símbolo</span><span class="sxs-lookup"><span data-stu-id="e593f-135">symbol</span></span>  | [<span data-ttu-id="e593f-136">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="e593f-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="e593f-137">O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="e593f-138">value</span><span class="sxs-lookup"><span data-stu-id="e593f-138">value</span></span>   | [<span data-ttu-id="e593f-139">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="e593f-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="e593f-140">O número a ser usado como o identificador da mensagem para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="e593f-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="e593f-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e593f-141">Remarks</span></span>

<span data-ttu-id="e593f-142">O limite prático do número de provedores que você pode definir em um manifesto é de 16 provedores.</span><span class="sxs-lookup"><span data-stu-id="e593f-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="e593f-143">Se você especificar mais de 16 provedores, deverá usar uma tabela de mensagens para atribuir explicitamente números de recursos às cadeias de caracteres de mensagens que o provedor referencia.</span><span class="sxs-lookup"><span data-stu-id="e593f-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="e593f-144">Para obter mais detalhes, consulte o elemento Message acima.</span><span class="sxs-lookup"><span data-stu-id="e593f-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="e593f-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e593f-145">Requirements</span></span>

| <span data-ttu-id="e593f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e593f-146">Requirement</span></span> | <span data-ttu-id="e593f-147">Valor</span><span class="sxs-lookup"><span data-stu-id="e593f-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="e593f-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e593f-148">Minimum supported client</span></span> | <span data-ttu-id="e593f-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e593f-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="e593f-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e593f-150">Minimum supported server</span></span> | <span data-ttu-id="e593f-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e593f-151">Windows Server 2008 \[desktop apps only\]</span></span> |
