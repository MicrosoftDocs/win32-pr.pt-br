---
title: Tipo complexo ValueMapValueType
description: Define o mapeamento entre um valor inteiro e um valor de cadeia de caracteres. | Tipo complexo ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- Log de eventos do tipo complexo ValueMapValueType
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370848"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="25845-105">Tipo complexo ValueMapValueType</span><span class="sxs-lookup"><span data-stu-id="25845-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="25845-106">Define o mapeamento entre um valor inteiro e um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="25845-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="25845-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="25845-107">Attributes</span></span>



| <span data-ttu-id="25845-108">Nome</span><span class="sxs-lookup"><span data-stu-id="25845-108">Name</span></span>    | <span data-ttu-id="25845-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="25845-109">Type</span></span>                                                              | <span data-ttu-id="25845-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="25845-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25845-111">message</span><span class="sxs-lookup"><span data-stu-id="25845-111">message</span></span> | [<span data-ttu-id="25845-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="25845-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="25845-113">O valor da cadeia de caracteres localizada para o qual o valor inteiro é mapeado.</span><span class="sxs-lookup"><span data-stu-id="25845-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="25845-114">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="25845-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="25845-115">símbolo</span><span class="sxs-lookup"><span data-stu-id="25845-115">symbol</span></span>  | [<span data-ttu-id="25845-116">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="25845-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="25845-117">O símbolo a ser usado para referenciar o mapa em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="25845-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="25845-118">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o mapa no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="25845-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="25845-119">Se você não especificar um símbolo, o compilador gerará um para você.</span><span class="sxs-lookup"><span data-stu-id="25845-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="25845-120">value</span><span class="sxs-lookup"><span data-stu-id="25845-120">value</span></span>   | [<span data-ttu-id="25845-121">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="25845-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="25845-122">O valor inteiro a ser mapeado para o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="25845-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="25845-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25845-123">Requirements</span></span>



| <span data-ttu-id="25845-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25845-124">Requirement</span></span> | <span data-ttu-id="25845-125">Valor</span><span class="sxs-lookup"><span data-stu-id="25845-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25845-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25845-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25845-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25845-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25845-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25845-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25845-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25845-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





