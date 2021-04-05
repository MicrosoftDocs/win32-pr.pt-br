---
description: Recupera uma matriz de bytes que contém os dados de propriedade internos e específicos do aplicativo para este IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Método IContextNode:: SavePropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920955"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="92204-103">Método IContextNode:: SavePropertiesData</span><span class="sxs-lookup"><span data-stu-id="92204-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="92204-104">Recupera uma matriz de bytes que contém os dados de propriedade internos e específicos do aplicativo para este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="92204-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92204-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92204-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="92204-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92204-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92204-107">*pulPropertiesDataSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="92204-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92204-108">O tamanho da matriz de dados que contém as informações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="92204-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="92204-109">O valor transmitido não é usado.</span><span class="sxs-lookup"><span data-stu-id="92204-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="92204-110">*ppbPropertiesData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="92204-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92204-111">Um ponteiro para uma matriz de inteiros sem sinal de 8 bits que contém os dados de propriedade internos e específicos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92204-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92204-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92204-112">Return value</span></span>

<span data-ttu-id="92204-113">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="92204-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92204-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="92204-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="92204-115">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppbPropertiesData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="92204-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="92204-116">Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="92204-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="92204-117">Esse método salva os dados de propriedade que o **IInkAnalyzer** definiu no [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="92204-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="92204-118">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="92204-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92204-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92204-119">Requirements</span></span>



| <span data-ttu-id="92204-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92204-120">Requirement</span></span> | <span data-ttu-id="92204-121">Valor</span><span class="sxs-lookup"><span data-stu-id="92204-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92204-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92204-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92204-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="92204-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="92204-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92204-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92204-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92204-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="92204-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92204-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92204-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="92204-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92204-128">DLL</span><span class="sxs-lookup"><span data-stu-id="92204-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92204-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92204-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="92204-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="92204-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92204-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="92204-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="92204-132">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="92204-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="92204-133">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="92204-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="92204-134">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="92204-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="92204-135">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="92204-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="92204-136">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="92204-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="92204-137">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="92204-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="92204-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="92204-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

