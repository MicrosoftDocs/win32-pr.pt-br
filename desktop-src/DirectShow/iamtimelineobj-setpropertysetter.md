---
description: O método SetPropertySetter define o setter da Propriedade do objeto. Quando o objeto é renderizado, as informações de propriedade contidas no setter da propriedade são aplicadas ao objeto. Chame esse método em objetos de transição e efeito.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Método IAMTimelineObj:: SetPropertySetter (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759549"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="fde43-105">Método IAMTimelineObj:: SetPropertySetter</span><span class="sxs-lookup"><span data-stu-id="fde43-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="fde43-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="fde43-106">\[Deprecated.</span></span> <span data-ttu-id="fde43-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fde43-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fde43-108">O `SetPropertySetter` método define o setter da Propriedade do objeto.</span><span class="sxs-lookup"><span data-stu-id="fde43-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="fde43-109">Quando o objeto é renderizado, as informações de propriedade contidas no setter da propriedade são aplicadas ao objeto.</span><span class="sxs-lookup"><span data-stu-id="fde43-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="fde43-110">Chame esse método em objetos de transição e efeito.</span><span class="sxs-lookup"><span data-stu-id="fde43-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde43-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fde43-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fde43-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fde43-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde43-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="fde43-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fde43-114">Ponteiro para a interface [**IPropertySetter**](ipropertysetter.md) do setter da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fde43-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde43-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fde43-115">Return value</span></span>

<span data-ttu-id="fde43-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fde43-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fde43-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fde43-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde43-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fde43-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fde43-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="fde43-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fde43-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fde43-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fde43-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fde43-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fde43-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde43-122">Requirements</span></span>



| <span data-ttu-id="fde43-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde43-123">Requirement</span></span> | <span data-ttu-id="fde43-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fde43-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde43-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fde43-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fde43-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde43-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fde43-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fde43-127">Library</span></span><br/> | <dl> <span data-ttu-id="fde43-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fde43-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde43-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fde43-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde43-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="fde43-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="fde43-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="fde43-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




