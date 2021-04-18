---
description: O método SetSubObjectGUID especifica o GUID do subobjeto associado a esse objeto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'Método IAMTimelineObj:: SetSubObjectGUID (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758060"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="12331-103">Método IAMTimelineObj:: SetSubObjectGUID</span><span class="sxs-lookup"><span data-stu-id="12331-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="12331-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="12331-104">\[Deprecated.</span></span> <span data-ttu-id="12331-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12331-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="12331-106">O `SetSubObjectGUID` método especifica o GUID do subobjeto associado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="12331-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12331-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12331-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="12331-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12331-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12331-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="12331-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="12331-110">GUID do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="12331-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12331-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12331-111">Return value</span></span>

<span data-ttu-id="12331-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="12331-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12331-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12331-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="12331-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="12331-114">Remarks</span></span>

<span data-ttu-id="12331-115">O mecanismo de processamento cria uma instância do subobjeto conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="12331-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="12331-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="12331-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="12331-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="12331-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="12331-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="12331-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12331-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12331-119">Requirements</span></span>



| <span data-ttu-id="12331-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12331-120">Requirement</span></span> | <span data-ttu-id="12331-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12331-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12331-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12331-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12331-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="12331-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="12331-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12331-124">Library</span></span><br/> | <dl> <span data-ttu-id="12331-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12331-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12331-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="12331-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12331-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="12331-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="12331-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="12331-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




