---
title: Selecionar elemento (QueryType)
description: Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Selecionar EventLog do elemento
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369860"
---
# <a name="select-querytype-element"></a><span data-ttu-id="5ed16-104">Selecionar elemento (QueryType)</span><span class="sxs-lookup"><span data-stu-id="5ed16-104">Select (QueryType) Element</span></span>

<span data-ttu-id="5ed16-105">Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="5ed16-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="5ed16-106">O elemento **Select** é definido pelo tipo complexo [**QueryType**](queryschema-querytype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed16-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="5ed16-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ed16-107">Attributes</span></span>



| <span data-ttu-id="5ed16-108">Nome</span><span class="sxs-lookup"><span data-stu-id="5ed16-108">Name</span></span> | <span data-ttu-id="5ed16-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ed16-109">Type</span></span>   | <span data-ttu-id="5ed16-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ed16-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed16-111">Caminho</span><span class="sxs-lookup"><span data-stu-id="5ed16-111">Path</span></span> | <span data-ttu-id="5ed16-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="5ed16-112">anyURI</span></span> | <span data-ttu-id="5ed16-113">O nome do canal ou o caminho para o arquivo de log que contém os eventos.</span><span class="sxs-lookup"><span data-stu-id="5ed16-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5ed16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed16-114">Requirements</span></span>



| <span data-ttu-id="5ed16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed16-115">Requirement</span></span> | <span data-ttu-id="5ed16-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed16-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5ed16-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed16-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ed16-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="5ed16-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ed16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed16-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5ed16-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ed16-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ed16-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ed16-122">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="5ed16-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="5ed16-123">**Consulta (QueryListType)**</span><span class="sxs-lookup"><span data-stu-id="5ed16-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





