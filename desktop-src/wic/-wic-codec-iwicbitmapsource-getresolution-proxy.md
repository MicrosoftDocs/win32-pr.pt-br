---
description: Função de proxy para o método getsolution.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: Função IWICBitmapSource_GetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169882"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="f88ed-103">Função de proxy de resolution de IWICBitmapSource \_ \_</span><span class="sxs-lookup"><span data-stu-id="f88ed-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="f88ed-104">Função de proxy para o método [**getsolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) .</span><span class="sxs-lookup"><span data-stu-id="f88ed-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f88ed-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="f88ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f88ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f88ed-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="f88ed-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ed-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="f88ed-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="f88ed-109">Ponteiro para este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="f88ed-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="f88ed-110">*pDpiX* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f88ed-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ed-111">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="f88ed-111">Type: \**double\** _</span></span>

<span data-ttu-id="f88ed-112">Um ponteiro que recebe a resolução de DPI do eixo x.</span><span class="sxs-lookup"><span data-stu-id="f88ed-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="f88ed-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f88ed-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f88ed-114">Tipo: \**Double \** _</span><span class="sxs-lookup"><span data-stu-id="f88ed-114">Type: \**double\** _</span></span>

<span data-ttu-id="f88ed-115">Um ponteiro que recebe a resolução de DPI do eixo y.</span><span class="sxs-lookup"><span data-stu-id="f88ed-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f88ed-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f88ed-116">Return value</span></span>

<span data-ttu-id="f88ed-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f88ed-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f88ed-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f88ed-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f88ed-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f88ed-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f88ed-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f88ed-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f88ed-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f88ed-121">Requirements</span></span>



| <span data-ttu-id="f88ed-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f88ed-122">Requirement</span></span> | <span data-ttu-id="f88ed-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f88ed-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f88ed-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f88ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f88ed-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f88ed-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f88ed-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f88ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f88ed-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f88ed-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f88ed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f88ed-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f88ed-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f88ed-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




