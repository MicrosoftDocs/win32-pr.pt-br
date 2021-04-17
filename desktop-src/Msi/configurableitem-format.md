---
description: A propriedade Format do objeto ConfigurableItem retorna o valor da coluna Format da Tabela ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Propriedade ConfigurableItem. Format (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747778"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="e53d5-103">Propriedade ConfigurableItem. Format</span><span class="sxs-lookup"><span data-stu-id="e53d5-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="e53d5-104">A propriedade **Format** do objeto [**ConfigurableItem**](configurableitem-object.md) retorna o valor da coluna Format da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="e53d5-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="e53d5-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e53d5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53d5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e53d5-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="e53d5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e53d5-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e53d5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e53d5-108">Remarks</span></span>

<span data-ttu-id="e53d5-109">Esta propriedade só pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e53d5-109">This property can only have the following values.</span></span>



| <span data-ttu-id="e53d5-110">Constante</span><span class="sxs-lookup"><span data-stu-id="e53d5-110">Constant</span></span>                        | <span data-ttu-id="e53d5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e53d5-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="e53d5-112">**msmConfigurableItemText**</span><span class="sxs-lookup"><span data-stu-id="e53d5-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="e53d5-113">0</span><span class="sxs-lookup"><span data-stu-id="e53d5-113">0</span></span>     |
| <span data-ttu-id="e53d5-114">**msmConfigurableItemKey**</span><span class="sxs-lookup"><span data-stu-id="e53d5-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="e53d5-115">1</span><span class="sxs-lookup"><span data-stu-id="e53d5-115">1</span></span>     |
| <span data-ttu-id="e53d5-116">**msmConfigurableItemInteger**</span><span class="sxs-lookup"><span data-stu-id="e53d5-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="e53d5-117">2</span><span class="sxs-lookup"><span data-stu-id="e53d5-117">2</span></span>     |
| <span data-ttu-id="e53d5-118">**msmConfigurableItemBitfield**</span><span class="sxs-lookup"><span data-stu-id="e53d5-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="e53d5-119">3</span><span class="sxs-lookup"><span data-stu-id="e53d5-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="e53d5-120">C++</span><span class="sxs-lookup"><span data-stu-id="e53d5-120">C++</span></span>

<span data-ttu-id="e53d5-121">Consulte [**obter \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) função de formato.</span><span class="sxs-lookup"><span data-stu-id="e53d5-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53d5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e53d5-122">Requirements</span></span>



| <span data-ttu-id="e53d5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e53d5-123">Requirement</span></span> | <span data-ttu-id="e53d5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e53d5-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e53d5-125">Versão</span><span class="sxs-lookup"><span data-stu-id="e53d5-125">Version</span></span><br/> | <span data-ttu-id="e53d5-126">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e53d5-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e53d5-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e53d5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e53d5-128"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e53d5-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e53d5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e53d5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="e53d5-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e53d5-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




