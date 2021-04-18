---
description: 'O método SetMediaLength2 especifica a duração do arquivo de origem. Esse método é equivalente a IAMTimelineSrc:: SetMediaLength, mas usa um valor de REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Método IAMTimelineSrc:: SetMediaLength2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779534"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="e13ed-104">Método IAMTimelineSrc:: SetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="e13ed-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="e13ed-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e13ed-105">\[Deprecated.</span></span> <span data-ttu-id="e13ed-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e13ed-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e13ed-107">O `SetMediaLength2` método especifica a duração do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="e13ed-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="e13ed-108">Esse método é equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e13ed-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13ed-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e13ed-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="e13ed-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e13ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13ed-111">*Comprimento*</span><span class="sxs-lookup"><span data-stu-id="e13ed-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="e13ed-112">Comprimento da mídia, em segundos.</span><span class="sxs-lookup"><span data-stu-id="e13ed-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13ed-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e13ed-113">Return value</span></span>

<span data-ttu-id="e13ed-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e13ed-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e13ed-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e13ed-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13ed-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e13ed-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e13ed-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e13ed-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e13ed-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e13ed-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e13ed-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e13ed-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e13ed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e13ed-120">Requirements</span></span>



| <span data-ttu-id="e13ed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e13ed-121">Requirement</span></span> | <span data-ttu-id="e13ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e13ed-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e13ed-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e13ed-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e13ed-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13ed-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e13ed-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e13ed-125">Library</span></span><br/> | <dl> <span data-ttu-id="e13ed-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e13ed-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13ed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e13ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13ed-128">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e13ed-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e13ed-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e13ed-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




