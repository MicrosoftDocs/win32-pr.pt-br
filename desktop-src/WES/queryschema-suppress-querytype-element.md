---
title: Elemento suprimir (QueryType)
description: Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Suprimir log de elemento
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086439"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="b6fc6-104">Elemento suprimir (QueryType)</span><span class="sxs-lookup"><span data-stu-id="b6fc6-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="b6fc6-105">Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="b6fc6-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b6fc6-106">O elemento **suprimir** é definido pelo tipo complexo [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b6fc6-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="b6fc6-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6fc6-107">Attributes</span></span>



| <span data-ttu-id="b6fc6-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b6fc6-108">Name</span></span> | <span data-ttu-id="b6fc6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6fc6-109">Type</span></span>   | <span data-ttu-id="b6fc6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6fc6-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6fc6-111">Caminho</span><span class="sxs-lookup"><span data-stu-id="b6fc6-111">Path</span></span> | <span data-ttu-id="b6fc6-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="b6fc6-112">anyURI</span></span> | <span data-ttu-id="b6fc6-113">O nome do canal ou o caminho para o arquivo de log que contém os eventos.</span><span class="sxs-lookup"><span data-stu-id="b6fc6-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b6fc6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6fc6-114">Requirements</span></span>



| <span data-ttu-id="b6fc6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6fc6-115">Requirement</span></span> | <span data-ttu-id="b6fc6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b6fc6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6fc6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fc6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6fc6-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6fc6-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6fc6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6fc6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6fc6-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6fc6-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6fc6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6fc6-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6fc6-122">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="b6fc6-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="b6fc6-123">**Consulta (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="b6fc6-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





