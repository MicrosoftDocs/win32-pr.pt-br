---
description: Define a seção do manifesto de instrumentação que identifica o provedor e os contadores que eles fornecem.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Tipo complexo de contadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921736"
---
# <a name="counters-complex-type"></a><span data-ttu-id="a8bd5-103">Tipo complexo de contadores</span><span class="sxs-lookup"><span data-stu-id="a8bd5-103">counters Complex Type</span></span>

<span data-ttu-id="a8bd5-104">Define a seção do manifesto de instrumentação que identifica o provedor e os contadores que eles fornecem.</span><span class="sxs-lookup"><span data-stu-id="a8bd5-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8bd5-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a8bd5-105">Child elements</span></span>



| <span data-ttu-id="a8bd5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8bd5-106">Element</span></span>      | <span data-ttu-id="a8bd5-107">Type</span><span class="sxs-lookup"><span data-stu-id="a8bd5-107">Type</span></span>                                                               | <span data-ttu-id="a8bd5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8bd5-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="a8bd5-109">**operador**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-109">**provider**</span></span> | [<span data-ttu-id="a8bd5-110">**Man: provedor**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="a8bd5-111">Identifica um provedor que fornece contadores.</span><span class="sxs-lookup"><span data-stu-id="a8bd5-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a8bd5-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8bd5-112">Attributes</span></span>



| <span data-ttu-id="a8bd5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="a8bd5-113">Name</span></span>          | <span data-ttu-id="a8bd5-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8bd5-114">Type</span></span> | <span data-ttu-id="a8bd5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8bd5-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="a8bd5-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="a8bd5-116">schemaVersion</span></span> |      | <span data-ttu-id="a8bd5-117">A versão do esquema usada para gravar o manifesto.</span><span class="sxs-lookup"><span data-stu-id="a8bd5-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8bd5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8bd5-118">Requirements</span></span>



| <span data-ttu-id="a8bd5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bd5-119">Requirement</span></span> | <span data-ttu-id="a8bd5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a8bd5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8bd5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8bd5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8bd5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8bd5-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8bd5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8bd5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8bd5-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8bd5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8bd5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8bd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bd5-126">**Instrumentação**</span><span class="sxs-lookup"><span data-stu-id="a8bd5-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

