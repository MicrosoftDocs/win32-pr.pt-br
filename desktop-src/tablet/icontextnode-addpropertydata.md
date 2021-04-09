---
description: Adiciona uma parte dos dados específicos do aplicativo.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'Método IContextNode:: AddPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090550"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="a80cf-103">Método IContextNode:: AddPropertyData</span><span class="sxs-lookup"><span data-stu-id="a80cf-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="a80cf-104">Adiciona uma parte dos dados específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a80cf-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80cf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a80cf-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="a80cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a80cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80cf-107">*pPropertyDataId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a80cf-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80cf-108">Um GUID (identificador global exclusivo) que é usado para identificar o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a80cf-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="a80cf-109">*ulPropertyDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a80cf-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80cf-110">O tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="a80cf-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a80cf-111">*pbPropertiesData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a80cf-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80cf-112">\[em, tamanho \_ é (ulPropertyDataSize)\]</span><span class="sxs-lookup"><span data-stu-id="a80cf-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="a80cf-113">Uma matriz de inteiros sem sinal de 8 bits que contém as informações de propriedade a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="a80cf-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80cf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a80cf-114">Return value</span></span>

<span data-ttu-id="a80cf-115">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a80cf-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a80cf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a80cf-116">Remarks</span></span>

<span data-ttu-id="a80cf-117">Use **IContextNode:: AddPropertyData** para associar dados a um nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="a80cf-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="a80cf-118">Para recuperar os dados mais tarde, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="a80cf-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="a80cf-119">O analisador de tinta pode excluir o nó como parte da análise de tinta, a menos que o nó de contexto seja confirmado (consulte [**IContextNode:: Confirm**](icontextnode-confirm.md)).</span><span class="sxs-lookup"><span data-stu-id="a80cf-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="a80cf-120">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a80cf-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a80cf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80cf-121">Requirements</span></span>



| <span data-ttu-id="a80cf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80cf-122">Requirement</span></span> | <span data-ttu-id="a80cf-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a80cf-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80cf-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80cf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a80cf-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a80cf-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a80cf-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80cf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a80cf-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a80cf-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a80cf-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a80cf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80cf-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a80cf-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a80cf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a80cf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a80cf-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a80cf-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a80cf-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a80cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80cf-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a80cf-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a80cf-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a80cf-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a80cf-135">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="a80cf-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="a80cf-136">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a80cf-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="a80cf-137">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a80cf-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a80cf-138">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="a80cf-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="a80cf-139">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a80cf-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




