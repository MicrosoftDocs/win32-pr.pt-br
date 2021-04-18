---
description: 'O método SetSubObjectGUIDB especifica o GUID do subobjeto associado a esse objeto. Esse método é equivalente a IAMTimelineObj:: SetSubObjectGUID, mas usa um valor BSTR.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'Método IAMTimelineObj:: SetSubObjectGUIDB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789684"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="8eb0e-104">Método IAMTimelineObj:: SetSubObjectGUIDB</span><span class="sxs-lookup"><span data-stu-id="8eb0e-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="8eb0e-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-105">\[Deprecated.</span></span> <span data-ttu-id="8eb0e-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8eb0e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8eb0e-107">O `SetSubObjectGUIDB` método especifica o GUID do subobjeto associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="8eb0e-108">Esse método é equivalente a [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) , mas usa um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="8eb0e-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb0e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eb0e-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="8eb0e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eb0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb0e-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="8eb0e-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb0e-112">**BSTR** que representa o GUID do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb0e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8eb0e-113">Return value</span></span>

<span data-ttu-id="8eb0e-114">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb0e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8eb0e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8eb0e-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8eb0e-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8eb0e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8eb0e-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8eb0e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8eb0e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eb0e-119">Requirements</span></span>



| <span data-ttu-id="8eb0e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eb0e-120">Requirement</span></span> | <span data-ttu-id="8eb0e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8eb0e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb0e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8eb0e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8eb0e-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eb0e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8eb0e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8eb0e-124">Library</span></span><br/> | <dl> <span data-ttu-id="8eb0e-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8eb0e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb0e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eb0e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb0e-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="8eb0e-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="8eb0e-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8eb0e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




