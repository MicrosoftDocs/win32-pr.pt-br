---
title: Propriedade DataType de IResultProperty (WdsSharedIDL. h)
description: Um tipo de dados de propriedades.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Propriedade DataType recursos de ambiente herdado do Windows
- Propriedade DataType recursos de ambiente herdados do Windows, interface IResultProperty
- Recursos do ambiente Windows herdado da interface IResultProperty, Propriedade DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765670"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="90a87-106">IResultProperty: Propriedade ataType de:D</span><span class="sxs-lookup"><span data-stu-id="90a87-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="90a87-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="90a87-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="90a87-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="90a87-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="90a87-109">Um tipo de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="90a87-109">A properties data type.</span></span>

<span data-ttu-id="90a87-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="90a87-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a87-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90a87-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="90a87-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="90a87-112">Property value</span></span>

<span data-ttu-id="90a87-113">Retorna um ponteiro para o tipo de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="90a87-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a87-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90a87-114">Requirements</span></span>



| <span data-ttu-id="90a87-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a87-115">Requirement</span></span> | <span data-ttu-id="90a87-116">Valor</span><span class="sxs-lookup"><span data-stu-id="90a87-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a87-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a87-117">Minimum supported client</span></span><br/> | <span data-ttu-id="90a87-118">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="90a87-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="90a87-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90a87-119">Minimum supported server</span></span><br/> | <span data-ttu-id="90a87-120">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="90a87-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="90a87-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="90a87-121">Redistributable</span></span><br/>          | <span data-ttu-id="90a87-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="90a87-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="90a87-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90a87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90a87-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="90a87-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





