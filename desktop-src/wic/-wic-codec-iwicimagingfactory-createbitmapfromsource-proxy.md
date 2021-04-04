---
description: Função de proxy para o método CreateBitmapFromSource.
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: Função IWICImagingFactory_CreateBitmapFromSource_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922923"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="74d1d-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapFromSource</span><span class="sxs-lookup"><span data-stu-id="74d1d-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="74d1d-104">Função de proxy para o método [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) .</span><span class="sxs-lookup"><span data-stu-id="74d1d-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d1d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74d1d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="74d1d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d1d-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d1d-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="74d1d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="74d1d-109">_pIBitmapSource \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d1d-110">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="74d1d-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="74d1d-111">O [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) do qual criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="74d1d-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="74d1d-112">*opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d1d-113">Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="74d1d-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="74d1d-114">As opções de cache do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="74d1d-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="74d1d-115">*ppIBitmap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74d1d-116">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="74d1d-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="74d1d-117">Um ponteiro que recebe um ponteiro para o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="74d1d-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d1d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74d1d-118">Return value</span></span>

<span data-ttu-id="74d1d-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74d1d-119">Type: **HRESULT**</span></span>

<span data-ttu-id="74d1d-120">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1d-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74d1d-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74d1d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74d1d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="74d1d-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="74d1d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74d1d-123">Requirements</span></span>



| <span data-ttu-id="74d1d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d1d-124">Requirement</span></span> | <span data-ttu-id="74d1d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="74d1d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d1d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74d1d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="74d1d-127">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="74d1d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74d1d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="74d1d-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74d1d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="74d1d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="74d1d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74d1d-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74d1d-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




