---
description: O método SetMediaTypeForVB especifica o tipo de mídia de grupo para clientes de automação.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Método IAMTimelineGroup:: SetMediaTypeForVB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760883"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="0fd5c-103">Método IAMTimelineGroup:: SetMediaTypeForVB</span><span class="sxs-lookup"><span data-stu-id="0fd5c-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="0fd5c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-104">\[Deprecated.</span></span> <span data-ttu-id="0fd5c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fd5c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0fd5c-106">O `SetMediaTypeForVB` método especifica o tipo de mídia de grupo para clientes de automação.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fd5c-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="0fd5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fd5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd5c-109">*Valor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0fd5c-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd5c-110">Valor que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-110">Value that specifies the media type.</span></span> <span data-ttu-id="0fd5c-111">Defina o valor como 0 para vídeo ou 1 para áudio.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd5c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fd5c-112">Return value</span></span>

<span data-ttu-id="0fd5c-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fd5c-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fd5c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd5c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fd5c-115">Remarks</span></span>

<span data-ttu-id="0fd5c-116">Esse método destina-se a clientes de automação.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="0fd5c-117">Para aplicativos C++, use o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd5c-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="0fd5c-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0fd5c-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0fd5c-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0fd5c-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0fd5c-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fd5c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd5c-121">Requirements</span></span>



| <span data-ttu-id="0fd5c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd5c-122">Requirement</span></span> | <span data-ttu-id="0fd5c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0fd5c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd5c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fd5c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0fd5c-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd5c-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0fd5c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0fd5c-126">Library</span></span><br/> | <dl> <span data-ttu-id="0fd5c-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fd5c-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd5c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd5c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd5c-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="0fd5c-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="0fd5c-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="0fd5c-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




