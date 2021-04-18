---
description: O método IsSmartRecompressFormatSet determina se um formato de recompactação inteligente foi definido para o grupo.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'Método IAMTimelineGroup:: IsSmartRecompressFormatSet (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757292"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="79b68-103">Método IAMTimelineGroup:: IsSmartRecompressFormatSet</span><span class="sxs-lookup"><span data-stu-id="79b68-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="79b68-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="79b68-104">\[Deprecated.</span></span> <span data-ttu-id="79b68-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79b68-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="79b68-106">O `IsSmartRecompressFormatSet` método determina se um formato de recompactação inteligente foi definido para o grupo.</span><span class="sxs-lookup"><span data-stu-id="79b68-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79b68-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="79b68-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79b68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79b68-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="79b68-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="79b68-110">Recebe um valor booliano que indica se um formato de compactação foi definido.</span><span class="sxs-lookup"><span data-stu-id="79b68-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="79b68-111">Se **for true**, um formato de compactação foi definido.</span><span class="sxs-lookup"><span data-stu-id="79b68-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79b68-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79b68-112">Return value</span></span>

<span data-ttu-id="79b68-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79b68-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79b68-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="79b68-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="79b68-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="79b68-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79b68-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="79b68-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="79b68-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="79b68-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="79b68-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="79b68-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79b68-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79b68-119">Requirements</span></span>



| <span data-ttu-id="79b68-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="79b68-120">Requirement</span></span> | <span data-ttu-id="79b68-121">Valor</span><span class="sxs-lookup"><span data-stu-id="79b68-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79b68-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79b68-122">Header</span></span><br/>  | <dl> <span data-ttu-id="79b68-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="79b68-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="79b68-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79b68-124">Library</span></span><br/> | <dl> <span data-ttu-id="79b68-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79b68-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79b68-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="79b68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b68-127">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="79b68-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="79b68-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="79b68-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




