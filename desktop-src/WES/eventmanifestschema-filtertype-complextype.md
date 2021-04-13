---
title: Tipo de filtro complexo
description: Define um filtro de dados que uma sessão usa para filtrar eventos com base nos dados do evento.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- LogType tipo complexo EventLog
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455999"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="10c1e-104">Tipo de filtro complexo</span><span class="sxs-lookup"><span data-stu-id="10c1e-104">FilterType Complex Type</span></span>

<span data-ttu-id="10c1e-105">Define um filtro de dados que uma sessão usa para filtrar eventos com base nos dados do evento.</span><span class="sxs-lookup"><span data-stu-id="10c1e-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="10c1e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="10c1e-106">Attributes</span></span>



| <span data-ttu-id="10c1e-107">Nome</span><span class="sxs-lookup"><span data-stu-id="10c1e-107">Name</span></span>    | <span data-ttu-id="10c1e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="10c1e-108">Type</span></span>                                                              | <span data-ttu-id="10c1e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="10c1e-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10c1e-110">message</span><span class="sxs-lookup"><span data-stu-id="10c1e-110">message</span></span> | [<span data-ttu-id="10c1e-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="10c1e-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="10c1e-112">A descrição localizada para o filtro.</span><span class="sxs-lookup"><span data-stu-id="10c1e-112">The localized description for the filter.</span></span> <span data-ttu-id="10c1e-113">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="10c1e-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="10c1e-114">name</span><span class="sxs-lookup"><span data-stu-id="10c1e-114">name</span></span>    | <span data-ttu-id="10c1e-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="10c1e-115">**QName**</span></span>                                                         | <span data-ttu-id="10c1e-116">Um nome que identifica o filtro.</span><span class="sxs-lookup"><span data-stu-id="10c1e-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="10c1e-117">símbolo</span><span class="sxs-lookup"><span data-stu-id="10c1e-117">symbol</span></span>  | [<span data-ttu-id="10c1e-118">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="10c1e-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="10c1e-119">O símbolo a ser usado para fazer referência ao filtro em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="10c1e-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="10c1e-120">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o filtro no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="10c1e-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="10c1e-121">tid</span><span class="sxs-lookup"><span data-stu-id="10c1e-121">tid</span></span>     | <span data-ttu-id="10c1e-122">token</span><span class="sxs-lookup"><span data-stu-id="10c1e-122">token</span></span>                                                             | <span data-ttu-id="10c1e-123">Um identificador de modelo que descreve os dados de filtro que a sessão passa para o provedor quando ele habilita o provedor.</span><span class="sxs-lookup"><span data-stu-id="10c1e-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="10c1e-124">value</span><span class="sxs-lookup"><span data-stu-id="10c1e-124">value</span></span>   | [<span data-ttu-id="10c1e-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="10c1e-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="10c1e-126">Um valor inteiro que identifica exclusivamente o filtro na lista de filtros que você define.</span><span class="sxs-lookup"><span data-stu-id="10c1e-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="10c1e-127">version</span><span class="sxs-lookup"><span data-stu-id="10c1e-127">version</span></span> | [<span data-ttu-id="10c1e-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="10c1e-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="10c1e-129">Um valor inteiro que identifica esta versão do filtro.</span><span class="sxs-lookup"><span data-stu-id="10c1e-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="10c1e-130">Se não for especificado, o valor será zero.</span><span class="sxs-lookup"><span data-stu-id="10c1e-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="10c1e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10c1e-131">Requirements</span></span>



| <span data-ttu-id="10c1e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c1e-132">Requirement</span></span> | <span data-ttu-id="10c1e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="10c1e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="10c1e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10c1e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="10c1e-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10c1e-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="10c1e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10c1e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="10c1e-137">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="10c1e-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





