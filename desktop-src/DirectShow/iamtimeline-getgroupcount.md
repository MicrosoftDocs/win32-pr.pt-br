---
description: O método GetGroupCount recupera o número de grupos contidos na linha do tempo.
ms.assetid: 24351e03-3132-4363-8171-eae517fb770a
title: 'Método IAMTimeline:: GetGroupCount (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroupCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4d16cf44839b05f39bc747cb89eda77842caa04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749816"
---
# <a name="iamtimelinegetgroupcount-method"></a><span data-ttu-id="9a232-103">Método IAMTimeline:: GetGroupCount</span><span class="sxs-lookup"><span data-stu-id="9a232-103">IAMTimeline::GetGroupCount method</span></span>

> [!Note]  
> <span data-ttu-id="9a232-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9a232-104">\[Deprecated.</span></span> <span data-ttu-id="9a232-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a232-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9a232-106">O `GetGroupCount` método recupera o número de grupos contidos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="9a232-106">The `GetGroupCount` method retrieves the number of groups that are contained in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a232-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a232-107">Syntax</span></span>


```C++
HRESULT GetGroupCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="9a232-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a232-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="9a232-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="9a232-110">Recebe o número de grupos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="9a232-110">Receives the number of groups in the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a232-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a232-111">Return value</span></span>

<span data-ttu-id="9a232-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a232-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a232-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a232-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a232-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a232-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a232-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9a232-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9a232-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9a232-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9a232-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9a232-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a232-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a232-118">Requirements</span></span>



| <span data-ttu-id="9a232-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a232-119">Requirement</span></span> | <span data-ttu-id="9a232-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a232-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a232-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a232-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9a232-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a232-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9a232-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a232-123">Library</span></span><br/> | <dl> <span data-ttu-id="9a232-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a232-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a232-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a232-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a232-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="9a232-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="9a232-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="9a232-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




