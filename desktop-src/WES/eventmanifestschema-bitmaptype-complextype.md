---
title: Tipo complexo de BitMaptype
description: Define uma lista de mapeamentos de nome/valor entre valores de bits e valores de cadeia de caracteres.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- EventLog do tipo complexo de BitMaptype
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455979"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="83b8e-104">Tipo complexo de BitMaptype</span><span class="sxs-lookup"><span data-stu-id="83b8e-104">BitMapType Complex Type</span></span>

<span data-ttu-id="83b8e-105">Define uma lista de mapeamentos de nome/valor entre valores de bits e valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="83b8e-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="83b8e-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="83b8e-106">Child elements</span></span>



| <span data-ttu-id="83b8e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="83b8e-107">Element</span></span>                                                   | <span data-ttu-id="83b8e-108">Type</span><span class="sxs-lookup"><span data-stu-id="83b8e-108">Type</span></span>                                                                       | <span data-ttu-id="83b8e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="83b8e-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="83b8e-110">**mapeada**</span><span class="sxs-lookup"><span data-stu-id="83b8e-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="83b8e-111">**BitMapValueType**</span><span class="sxs-lookup"><span data-stu-id="83b8e-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="83b8e-112">Define o mapeamento entre um valor de bit e um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="83b8e-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="83b8e-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="83b8e-113">Attributes</span></span>



| <span data-ttu-id="83b8e-114">Nome</span><span class="sxs-lookup"><span data-stu-id="83b8e-114">Name</span></span>   | <span data-ttu-id="83b8e-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="83b8e-115">Type</span></span>                                                              | <span data-ttu-id="83b8e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="83b8e-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b8e-117">name</span><span class="sxs-lookup"><span data-stu-id="83b8e-117">name</span></span>   | <span data-ttu-id="83b8e-118">string</span><span class="sxs-lookup"><span data-stu-id="83b8e-118">string</span></span>                                                            | <span data-ttu-id="83b8e-119">O nome do bitmap.</span><span class="sxs-lookup"><span data-stu-id="83b8e-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="83b8e-120">símbolo</span><span class="sxs-lookup"><span data-stu-id="83b8e-120">symbol</span></span> | [<span data-ttu-id="83b8e-121">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="83b8e-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="83b8e-122">O símbolo a ser usado para fazer referência aos mapeamentos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="83b8e-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="83b8e-123">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="83b8e-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="83b8e-124">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="83b8e-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="83b8e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83b8e-125">Requirements</span></span>



| <span data-ttu-id="83b8e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b8e-126">Requirement</span></span> | <span data-ttu-id="83b8e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="83b8e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83b8e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83b8e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83b8e-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83b8e-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83b8e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83b8e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83b8e-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83b8e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





