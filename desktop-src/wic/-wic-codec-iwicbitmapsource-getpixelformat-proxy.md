---
description: Função de proxy para o método GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Função IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784552"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="9eec5-103">\_Função de proxy IWICBitmapSource GetPixelFormat \_</span><span class="sxs-lookup"><span data-stu-id="9eec5-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="9eec5-104">Função de proxy para o método [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .</span><span class="sxs-lookup"><span data-stu-id="9eec5-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eec5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eec5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="9eec5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eec5-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9eec5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eec5-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9eec5-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9eec5-109">Ponteiro para este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="9eec5-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="9eec5-110">*pPixelFormat* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9eec5-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eec5-111">Tipo: \**WICPixelFormatGUID \** _</span><span class="sxs-lookup"><span data-stu-id="9eec5-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="9eec5-112">Um ponteiro que recebe o formato de pixel GUID no qual o bitmap está armazenado.</span><span class="sxs-lookup"><span data-stu-id="9eec5-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eec5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eec5-113">Return value</span></span>

<span data-ttu-id="9eec5-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9eec5-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9eec5-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9eec5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9eec5-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9eec5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eec5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eec5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9eec5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eec5-118">Requirements</span></span>



| <span data-ttu-id="9eec5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eec5-119">Requirement</span></span> | <span data-ttu-id="9eec5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9eec5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eec5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eec5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9eec5-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9eec5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9eec5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eec5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9eec5-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9eec5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9eec5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9eec5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eec5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eec5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




