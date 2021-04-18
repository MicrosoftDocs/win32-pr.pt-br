---
description: 'Recria os dados de propriedade interna e específica do aplicativo para uma matriz de bytes que foi criada anteriormente com IContextNode:: SavePropertiesData.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'Método IContextNode:: LoadPropertiesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788837"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="84491-103">Método IContextNode:: LoadPropertiesData</span><span class="sxs-lookup"><span data-stu-id="84491-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="84491-104">Recria os dados de propriedade interna e específica do aplicativo para uma matriz de bytes que foi criada anteriormente com [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="84491-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84491-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84491-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="84491-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84491-107">*cbPropertiesDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84491-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84491-108">O tamanho da matriz de dados de propriedades.</span><span class="sxs-lookup"><span data-stu-id="84491-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="84491-109">*pbPropertiesData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84491-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84491-110">A matriz de inteiros sem sinal de 8 bits que contém as informações de propriedade a serem carregadas.</span><span class="sxs-lookup"><span data-stu-id="84491-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="84491-111">*pfSuccessful* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84491-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84491-112">**Variante \_ TRUE** se os dados de propriedade forem carregados com êxito; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="84491-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84491-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84491-113">Return value</span></span>

<span data-ttu-id="84491-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="84491-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84491-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84491-115">Requirements</span></span>



| <span data-ttu-id="84491-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84491-116">Requirement</span></span> | <span data-ttu-id="84491-117">Valor</span><span class="sxs-lookup"><span data-stu-id="84491-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84491-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84491-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84491-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="84491-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="84491-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84491-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84491-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84491-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="84491-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84491-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84491-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="84491-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="84491-124">DLL</span><span class="sxs-lookup"><span data-stu-id="84491-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84491-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84491-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="84491-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="84491-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84491-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="84491-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="84491-128">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="84491-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="84491-129">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="84491-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="84491-130">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="84491-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="84491-131">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="84491-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="84491-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="84491-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="84491-133">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="84491-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="84491-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="84491-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




