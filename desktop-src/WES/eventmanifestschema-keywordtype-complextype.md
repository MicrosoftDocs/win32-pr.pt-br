---
title: Tipo complexo keywordtype
description: Define uma palavra-chave que identifica uma categoria de eventos. | Tipo complexo keywordtype
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- EventLog de tipo complexo de keywordtype
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105759769"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="c3a18-105">Tipo complexo keywordtype</span><span class="sxs-lookup"><span data-stu-id="c3a18-105">KeywordType Complex Type</span></span>

<span data-ttu-id="c3a18-106">Define uma palavra-chave que identifica uma categoria de eventos.</span><span class="sxs-lookup"><span data-stu-id="c3a18-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="c3a18-107">Uma palavra-chave é uma marca que você anexa a um evento para agrupar eventos com base em seu uso.</span><span class="sxs-lookup"><span data-stu-id="c3a18-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="c3a18-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3a18-108">Attributes</span></span>



| <span data-ttu-id="c3a18-109">Nome</span><span class="sxs-lookup"><span data-stu-id="c3a18-109">Name</span></span>    | <span data-ttu-id="c3a18-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3a18-110">Type</span></span>                                                              | <span data-ttu-id="c3a18-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a18-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a18-112">mask</span><span class="sxs-lookup"><span data-stu-id="c3a18-112">mask</span></span>    | [<span data-ttu-id="c3a18-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="c3a18-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="c3a18-114">Um bitmask que deve ter apenas um único conjunto de bits.</span><span class="sxs-lookup"><span data-stu-id="c3a18-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="c3a18-115">O bit representa uma categoria de eventos (por exemplo, eventos de leitura ou eventos de gravação).</span><span class="sxs-lookup"><span data-stu-id="c3a18-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="c3a18-116">Você pode especificar valores de bit no intervalo de 0x0000000000000001 a 0x0000800000000000 (bits 0 a 47).</span><span class="sxs-lookup"><span data-stu-id="c3a18-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="c3a18-117">message</span><span class="sxs-lookup"><span data-stu-id="c3a18-117">message</span></span> | [<span data-ttu-id="c3a18-118">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="c3a18-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="c3a18-119">O nome de exibição localizado para a palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="c3a18-119">The localized display name for the keyword.</span></span> <span data-ttu-id="c3a18-120">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="c3a18-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="c3a18-121">name</span><span class="sxs-lookup"><span data-stu-id="c3a18-121">name</span></span>    | <span data-ttu-id="c3a18-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="c3a18-122">**QName**</span></span>                                                         | <span data-ttu-id="c3a18-123">O nome da palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="c3a18-123">The name of the keyword.</span></span> <span data-ttu-id="c3a18-124">O nome deve ser exclusivo na lista de palavras-chave que o provedor define.</span><span class="sxs-lookup"><span data-stu-id="c3a18-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="c3a18-125">símbolo</span><span class="sxs-lookup"><span data-stu-id="c3a18-125">symbol</span></span>  | [<span data-ttu-id="c3a18-126">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="c3a18-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="c3a18-127">O símbolo a ser usado para referenciar a palavra-chave em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3a18-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="c3a18-128">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para a palavra-chave no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="c3a18-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="c3a18-129">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="c3a18-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c3a18-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a18-130">Remarks</span></span>

<span data-ttu-id="c3a18-131">O arquivo de Winmeta.xml que está incluído no SDK do Windows contém uma lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c3a18-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="c3a18-132">Essas palavras-chave são reservadas e não devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="c3a18-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a18-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a18-133">Requirements</span></span>



| <span data-ttu-id="c3a18-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a18-134">Requirement</span></span> | <span data-ttu-id="c3a18-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a18-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3a18-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3a18-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a18-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3a18-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3a18-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3a18-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a18-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3a18-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





