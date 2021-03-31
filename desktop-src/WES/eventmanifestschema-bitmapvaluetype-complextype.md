---
title: Tipo complexo BitMapValueType
description: Define o mapeamento entre um valor de bit e um valor de cadeia de caracteres. | Tipo complexo BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Log de eventos do tipo complexo BitMapValueType
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930390"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="b014d-105">Tipo complexo BitMapValueType</span><span class="sxs-lookup"><span data-stu-id="b014d-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="b014d-106">Define o mapeamento entre um valor de bit e um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b014d-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b014d-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b014d-107">Attributes</span></span>



| <span data-ttu-id="b014d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b014d-108">Name</span></span>    | <span data-ttu-id="b014d-109">Type</span><span class="sxs-lookup"><span data-stu-id="b014d-109">Type</span></span>                                                              | <span data-ttu-id="b014d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b014d-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b014d-111">message</span><span class="sxs-lookup"><span data-stu-id="b014d-111">message</span></span> | [<span data-ttu-id="b014d-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="b014d-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b014d-113">O valor da cadeia de caracteres localizada para o qual o valor de bits é mapeado.</span><span class="sxs-lookup"><span data-stu-id="b014d-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="b014d-114">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="b014d-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="b014d-115">símbolo</span><span class="sxs-lookup"><span data-stu-id="b014d-115">symbol</span></span>  | [<span data-ttu-id="b014d-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="b014d-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b014d-117">O símbolo a ser usado para referenciar o mapa em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b014d-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="b014d-118">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="b014d-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="b014d-119">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="b014d-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="b014d-120">value</span><span class="sxs-lookup"><span data-stu-id="b014d-120">value</span></span>   | [<span data-ttu-id="b014d-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b014d-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="b014d-122">O valor de bit a ser mapeado para o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b014d-122">The bit value to map to the string value.</span></span> <span data-ttu-id="b014d-123">Você deve especificar um número hexadecimal que tenha um único conjunto de bits.</span><span class="sxs-lookup"><span data-stu-id="b014d-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="b014d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b014d-124">Remarks</span></span>

<span data-ttu-id="b014d-125">Mapeia um valor hexadecimal (o número deve ser precedido por 0x) com um único bit definido como um nome.</span><span class="sxs-lookup"><span data-stu-id="b014d-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b014d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b014d-126">Requirements</span></span>



| <span data-ttu-id="b014d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b014d-127">Requirement</span></span> | <span data-ttu-id="b014d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b014d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b014d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b014d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b014d-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b014d-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b014d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b014d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b014d-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b014d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





