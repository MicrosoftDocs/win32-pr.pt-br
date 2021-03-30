---
title: Tipo complexo ValueMapType
description: Define uma lista de mapeamentos de nome/valor entre valores inteiros e valores de cadeia de caracteres.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- Log de eventos do tipo complexo ValueMapType
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644203"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="964c3-104">Tipo complexo ValueMapType</span><span class="sxs-lookup"><span data-stu-id="964c3-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="964c3-105">Define uma lista de mapeamentos de nome/valor entre valores inteiros e valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="964c3-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="964c3-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="964c3-106">Child elements</span></span>



| <span data-ttu-id="964c3-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="964c3-107">Element</span></span>                                                     | <span data-ttu-id="964c3-108">Type</span><span class="sxs-lookup"><span data-stu-id="964c3-108">Type</span></span>                                                                           | <span data-ttu-id="964c3-109">Description</span><span class="sxs-lookup"><span data-stu-id="964c3-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="964c3-110">**mapeada**</span><span class="sxs-lookup"><span data-stu-id="964c3-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="964c3-111">**ValueMapValueType**</span><span class="sxs-lookup"><span data-stu-id="964c3-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="964c3-112">Define o mapeamento entre um valor inteiro e um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="964c3-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="964c3-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="964c3-113">Attributes</span></span>



| <span data-ttu-id="964c3-114">Nome</span><span class="sxs-lookup"><span data-stu-id="964c3-114">Name</span></span>   | <span data-ttu-id="964c3-115">Type</span><span class="sxs-lookup"><span data-stu-id="964c3-115">Type</span></span>                                                              | <span data-ttu-id="964c3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="964c3-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="964c3-117">name</span><span class="sxs-lookup"><span data-stu-id="964c3-117">name</span></span>   | <span data-ttu-id="964c3-118">string</span><span class="sxs-lookup"><span data-stu-id="964c3-118">string</span></span>                                                            | <span data-ttu-id="964c3-119">O nome do mapa de valor.</span><span class="sxs-lookup"><span data-stu-id="964c3-119">The name of the value map.</span></span> <span data-ttu-id="964c3-120">Use o nome em um elemento de dados para fazer referência aos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="964c3-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="964c3-121">símbolo</span><span class="sxs-lookup"><span data-stu-id="964c3-121">symbol</span></span> | [<span data-ttu-id="964c3-122">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="964c3-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="964c3-123">O símbolo a ser usado para fazer referência aos mapeamentos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="964c3-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="964c3-124">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="964c3-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="964c3-125">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="964c3-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="964c3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="964c3-126">Requirements</span></span>



| <span data-ttu-id="964c3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="964c3-127">Requirement</span></span> | <span data-ttu-id="964c3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="964c3-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="964c3-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="964c3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="964c3-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="964c3-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="964c3-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="964c3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="964c3-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="964c3-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





