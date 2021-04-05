---
description: Especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Elemento Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827211"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="bff94-103">Elemento Compression (contextType)</span><span class="sxs-lookup"><span data-stu-id="bff94-103">Compression (contextType) Element</span></span>

<span data-ttu-id="bff94-104">O elemento **Compression (ContextType)** especifica se a compactação será usada no link de dados para a transferência de dados e de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="bff94-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="bff94-105">Esse elemento pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bff94-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="bff94-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bff94-106">Value</span></span>     | <span data-ttu-id="bff94-107">Significado</span><span class="sxs-lookup"><span data-stu-id="bff94-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="bff94-108">DESABILITAR</span><span class="sxs-lookup"><span data-stu-id="bff94-108">"ENABLE"</span></span>  | <span data-ttu-id="bff94-109">A compactação será usada.</span><span class="sxs-lookup"><span data-stu-id="bff94-109">Compression will be used.</span></span>     |
| <span data-ttu-id="bff94-110">DESATIVAR</span><span class="sxs-lookup"><span data-stu-id="bff94-110">"DISABLE"</span></span> | <span data-ttu-id="bff94-111">A compactação não será usada.</span><span class="sxs-lookup"><span data-stu-id="bff94-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="bff94-112">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="bff94-112">This element is optional.</span></span> <span data-ttu-id="bff94-113">Se esse elemento não for especificado, o sistema de banda larga móvel não usará a compactação.</span><span class="sxs-lookup"><span data-stu-id="bff94-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bff94-114">O elemento **Compression** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bff94-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff94-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bff94-115">Requirements</span></span>



| <span data-ttu-id="bff94-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff94-116">Requirement</span></span> | <span data-ttu-id="bff94-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bff94-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bff94-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bff94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bff94-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bff94-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bff94-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bff94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bff94-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bff94-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bff94-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bff94-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="bff94-123">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="bff94-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bff94-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="bff94-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="bff94-125">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="bff94-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bff94-126">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="bff94-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




