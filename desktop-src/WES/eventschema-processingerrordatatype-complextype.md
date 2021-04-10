---
title: Tipo complexo ProcessingErrorDataType
description: Define um erro que ocorreu ao renderizar os dados de evento para o evento.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Log de eventos do tipo complexo ProcessingErrorDataType
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086055"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="65c6d-104">Tipo complexo ProcessingErrorDataType</span><span class="sxs-lookup"><span data-stu-id="65c6d-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="65c6d-105">Define um erro que ocorreu ao renderizar os dados de evento para o evento.</span><span class="sxs-lookup"><span data-stu-id="65c6d-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="65c6d-106">Isso pode ocorrer se os dados do evento não corresponderem à definição do modelo de dados do evento no manifesto.</span><span class="sxs-lookup"><span data-stu-id="65c6d-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="65c6d-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="65c6d-107">Child elements</span></span>



| <span data-ttu-id="65c6d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="65c6d-108">Element</span></span>                                                                          | <span data-ttu-id="65c6d-109">Type</span><span class="sxs-lookup"><span data-stu-id="65c6d-109">Type</span></span>        | <span data-ttu-id="65c6d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="65c6d-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="65c6d-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="65c6d-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="65c6d-112">string</span><span class="sxs-lookup"><span data-stu-id="65c6d-112">string</span></span>      | <span data-ttu-id="65c6d-113">O nome do item de dados de evento que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="65c6d-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="65c6d-114">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="65c6d-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="65c6d-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65c6d-115">unsignedInt</span></span> | <span data-ttu-id="65c6d-116">O código de erro do erro que ocorreu ao renderizar os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="65c6d-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="65c6d-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="65c6d-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="65c6d-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="65c6d-118">hexBinary</span></span>   | <span data-ttu-id="65c6d-119">Um blob binário que contém os dados de evento inteiros.</span><span class="sxs-lookup"><span data-stu-id="65c6d-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="65c6d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65c6d-120">Requirements</span></span>



| <span data-ttu-id="65c6d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="65c6d-121">Requirement</span></span> | <span data-ttu-id="65c6d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65c6d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="65c6d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65c6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65c6d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65c6d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="65c6d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65c6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65c6d-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65c6d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





