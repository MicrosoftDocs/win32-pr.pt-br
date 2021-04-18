---
title: Tipo complexo XmlTypeListType
description: Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Log de eventos do tipo complexo XmlTypeListType
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295807"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="60b16-104">Tipo complexo XmlTypeListType</span><span class="sxs-lookup"><span data-stu-id="60b16-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="60b16-105">Define uma lista de tipos de saída que o serviço usa para determinar como renderizar um tipo de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="60b16-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="60b16-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="60b16-106">Child elements</span></span>



| <span data-ttu-id="60b16-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="60b16-107">Element</span></span>                                                                | <span data-ttu-id="60b16-108">Type</span><span class="sxs-lookup"><span data-stu-id="60b16-108">Type</span></span> | <span data-ttu-id="60b16-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="60b16-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="60b16-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="60b16-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="60b16-111">Define um tipo XML.</span><span class="sxs-lookup"><span data-stu-id="60b16-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="60b16-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="60b16-112">Attributes</span></span>



| <span data-ttu-id="60b16-113">Nome</span><span class="sxs-lookup"><span data-stu-id="60b16-113">Name</span></span>   | <span data-ttu-id="60b16-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="60b16-114">Type</span></span>                                                              | <span data-ttu-id="60b16-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="60b16-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b16-116">name</span><span class="sxs-lookup"><span data-stu-id="60b16-116">name</span></span>   | <span data-ttu-id="60b16-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="60b16-117">**QName**</span></span>                                                         | <span data-ttu-id="60b16-118">O nome do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="60b16-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="60b16-119">símbolo</span><span class="sxs-lookup"><span data-stu-id="60b16-119">symbol</span></span> | [<span data-ttu-id="60b16-120">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="60b16-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="60b16-121">O símbolo a ser usado para referenciar o tipo de saída em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60b16-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="60b16-122">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o tipo de saída no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="60b16-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="60b16-123">value</span><span class="sxs-lookup"><span data-stu-id="60b16-123">value</span></span>  | <span data-ttu-id="60b16-124">string</span><span class="sxs-lookup"><span data-stu-id="60b16-124">string</span></span>                                                            | <span data-ttu-id="60b16-125">Um valor inteiro que identifica exclusivamente o tipo de saída na lista de tipos de saída que você define.</span><span class="sxs-lookup"><span data-stu-id="60b16-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="60b16-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="60b16-126">Remarks</span></span>

<span data-ttu-id="60b16-127">O \\ arquivo de inclusão \\Winmeta.xml, que está incluído na SDK do Windows, contém uma lista de tipos de saída predefinidos.</span><span class="sxs-lookup"><span data-stu-id="60b16-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b16-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b16-128">Requirements</span></span>



| <span data-ttu-id="60b16-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="60b16-129">Requirement</span></span> | <span data-ttu-id="60b16-130">Valor</span><span class="sxs-lookup"><span data-stu-id="60b16-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60b16-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60b16-131">Minimum supported client</span></span><br/> | <span data-ttu-id="60b16-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60b16-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60b16-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60b16-133">Minimum supported server</span></span><br/> | <span data-ttu-id="60b16-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60b16-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





