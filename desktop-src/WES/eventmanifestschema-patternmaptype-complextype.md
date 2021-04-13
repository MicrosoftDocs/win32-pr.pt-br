---
title: Tipo complexo PatternMapType
description: Não usado. Define um mapeamento entre duas expressões regulares. Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres de mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres de mensagem.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- Log de eventos do tipo complexo PatternMapType
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455371"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="51bff-106">Tipo complexo PatternMapType</span><span class="sxs-lookup"><span data-stu-id="51bff-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="51bff-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="51bff-107">Not used.</span></span> <span data-ttu-id="51bff-108">Define um mapeamento entre duas expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="51bff-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="51bff-109">Uma expressão é usada para localizar uma cadeia de caracteres correspondente na cadeia de caracteres de mensagem e a outra é usada para alterar a cadeia de caracteres antes que o serviço a Coloque novamente na cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="51bff-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="51bff-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="51bff-110">Child elements</span></span>



| <span data-ttu-id="51bff-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="51bff-111">Element</span></span>                                                       | <span data-ttu-id="51bff-112">Type</span><span class="sxs-lookup"><span data-stu-id="51bff-112">Type</span></span>                                                                               | <span data-ttu-id="51bff-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="51bff-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51bff-114">**mapeada**</span><span class="sxs-lookup"><span data-stu-id="51bff-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="51bff-115">**PatternMapValueType**</span><span class="sxs-lookup"><span data-stu-id="51bff-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="51bff-116">Define as expressões regulares usadas para localizar uma cadeia de caracteres correspondente na cadeia de caracteres da mensagem e alterá-la.</span><span class="sxs-lookup"><span data-stu-id="51bff-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="51bff-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="51bff-117">Attributes</span></span>



| <span data-ttu-id="51bff-118">Nome</span><span class="sxs-lookup"><span data-stu-id="51bff-118">Name</span></span>   | <span data-ttu-id="51bff-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="51bff-119">Type</span></span>                                                              | <span data-ttu-id="51bff-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="51bff-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bff-121">format</span><span class="sxs-lookup"><span data-stu-id="51bff-121">format</span></span> | <span data-ttu-id="51bff-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="51bff-122">anyURI</span></span>                                                            | <span data-ttu-id="51bff-123">O mecanismo de expressão regular a ser usado.</span><span class="sxs-lookup"><span data-stu-id="51bff-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="51bff-124">name</span><span class="sxs-lookup"><span data-stu-id="51bff-124">name</span></span>   | <span data-ttu-id="51bff-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="51bff-125">**QName**</span></span>                                                         | <span data-ttu-id="51bff-126">O nome do mapa de padrão.</span><span class="sxs-lookup"><span data-stu-id="51bff-126">The name of the pattern map.</span></span> <span data-ttu-id="51bff-127">Use o nome em um elemento de dados para fazer referência aos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="51bff-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="51bff-128">símbolo</span><span class="sxs-lookup"><span data-stu-id="51bff-128">symbol</span></span> | [<span data-ttu-id="51bff-129">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="51bff-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="51bff-130">O símbolo a ser usado para fazer referência aos mapeamentos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="51bff-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="51bff-131">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="51bff-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="51bff-132">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="51bff-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="51bff-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51bff-133">Requirements</span></span>



| <span data-ttu-id="51bff-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="51bff-134">Requirement</span></span> | <span data-ttu-id="51bff-135">Valor</span><span class="sxs-lookup"><span data-stu-id="51bff-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51bff-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bff-136">Minimum supported client</span></span><br/> | <span data-ttu-id="51bff-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51bff-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51bff-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51bff-138">Minimum supported server</span></span><br/> | <span data-ttu-id="51bff-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51bff-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





