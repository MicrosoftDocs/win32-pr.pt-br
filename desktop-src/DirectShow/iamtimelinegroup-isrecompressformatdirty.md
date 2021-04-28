---
description: 'Método IAMTimelineGroup:: IsRecompressFormatDirty-sem suporte.'
ms.assetid: 4fd6b9d9-1749-44e6-884a-16faeced4ed6
title: 'Método IAMTimelineGroup:: IsRecompressFormatDirty (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsRecompressFormatDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 842b4178f93505a2848fa01aa055541943fb3c22
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098614"
---
# <a name="iamtimelinegroupisrecompressformatdirty-method"></a><span data-ttu-id="04492-103">Método IAMTimelineGroup:: IsRecompressFormatDirty</span><span class="sxs-lookup"><span data-stu-id="04492-103">IAMTimelineGroup::IsRecompressFormatDirty method</span></span>

> [!Note]  
> <span data-ttu-id="04492-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="04492-104">\[Deprecated.</span></span> <span data-ttu-id="04492-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04492-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04492-106">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="04492-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="04492-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04492-107">Syntax</span></span>


```C++
HRESULT IsRecompressFormatDirty(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="04492-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04492-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04492-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="04492-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="04492-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="04492-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04492-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="04492-111">Return value</span></span>

<span data-ttu-id="04492-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04492-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04492-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04492-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04492-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04492-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="04492-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="04492-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04492-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04492-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04492-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="04492-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04492-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04492-118">Requirements</span></span>



| <span data-ttu-id="04492-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04492-119">Requirement</span></span> | <span data-ttu-id="04492-120">Valor</span><span class="sxs-lookup"><span data-stu-id="04492-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04492-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04492-121">Header</span></span><br/>  | <dl> <span data-ttu-id="04492-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="04492-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04492-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04492-123">Library</span></span><br/> | <dl> <span data-ttu-id="04492-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04492-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04492-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="04492-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04492-126">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="04492-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> </dl>

 

 




