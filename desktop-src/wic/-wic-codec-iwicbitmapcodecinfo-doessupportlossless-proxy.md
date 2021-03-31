---
description: Função de proxy para o método DoesSupportLossless.
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: Função IWICBitmapCodecInfo_DoesSupportLossless_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f498af72391aa0a7745ed79d06c6e1d55317393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647086"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a><span data-ttu-id="c41c3-103">\_Função de \_ proxy IWICBitmapCodecInfo DoesSupportLossless</span><span class="sxs-lookup"><span data-stu-id="c41c3-103">IWICBitmapCodecInfo\_DoesSupportLossless\_Proxy function</span></span>

<span data-ttu-id="c41c3-104">Função de proxy para o método [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) .</span><span class="sxs-lookup"><span data-stu-id="c41c3-104">Proxy function for the [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c41c3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a><span data-ttu-id="c41c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c41c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41c3-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c41c3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41c3-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c41c3-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="c41c3-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="c41c3-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c41c3-110">*pfSupportLossless* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c41c3-110">*pfSupportLossless* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c41c3-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="c41c3-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="c41c3-112">Um ponteiro que recebe _ *true*\* se o codec oferece suporte a formatos sem perdas; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="c41c3-112">A pointer that receives _ *TRUE*\* if the codec supports lossless formats; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41c3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c41c3-113">Return value</span></span>

<span data-ttu-id="c41c3-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c41c3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c41c3-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c41c3-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c41c3-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c41c3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c41c3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c41c3-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c41c3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c41c3-118">Requirements</span></span>



| <span data-ttu-id="c41c3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c41c3-119">Requirement</span></span> | <span data-ttu-id="c41c3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c41c3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41c3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c41c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c41c3-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c41c3-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c41c3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c41c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c41c3-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c41c3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c41c3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c41c3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c41c3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c41c3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




