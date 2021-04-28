---
description: Função IWICBitmapScaler_Initialize_Proxy function-proxy para o método Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: Função IWICBitmapScaler_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 76b7c754273f4d55fbf3de9d8ba592806e590aac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100534"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="46457-103">Função de proxy de \_ inicialização IWICBitmapScaler \_</span><span class="sxs-lookup"><span data-stu-id="46457-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="46457-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="46457-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46457-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46457-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="46457-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46457-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46457-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="46457-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46457-108">Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span><span class="sxs-lookup"><span data-stu-id="46457-108">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\***</span></span>

<span data-ttu-id="46457-109">Ponteiro para este objeto [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="46457-109">Pointer to this [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="46457-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46457-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46457-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="46457-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="46457-112">A origem do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="46457-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="46457-113">*uiWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46457-113">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46457-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="46457-114">Type: **UINT**</span></span>

<span data-ttu-id="46457-115">A largura de destino.</span><span class="sxs-lookup"><span data-stu-id="46457-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="46457-116">*uiHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46457-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46457-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="46457-117">Type: **UINT**</span></span>

<span data-ttu-id="46457-118">A altura de destino.</span><span class="sxs-lookup"><span data-stu-id="46457-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="46457-119">*modo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46457-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46457-120">Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="46457-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="46457-121">O modo de interpolação a ser usado ao Dimensionar.</span><span class="sxs-lookup"><span data-stu-id="46457-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46457-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="46457-122">Return value</span></span>

<span data-ttu-id="46457-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46457-123">Type: **HRESULT**</span></span>

<span data-ttu-id="46457-124">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46457-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46457-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46457-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46457-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="46457-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="46457-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46457-127">Requirements</span></span>



| <span data-ttu-id="46457-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="46457-128">Requirement</span></span> | <span data-ttu-id="46457-129">Valor</span><span class="sxs-lookup"><span data-stu-id="46457-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46457-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46457-130">Minimum supported client</span></span><br/> | <span data-ttu-id="46457-131">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46457-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="46457-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46457-132">Minimum supported server</span></span><br/> | <span data-ttu-id="46457-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46457-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="46457-134">DLL</span><span class="sxs-lookup"><span data-stu-id="46457-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46457-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46457-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




