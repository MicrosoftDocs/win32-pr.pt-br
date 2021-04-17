---
description: Função de proxy para o método Initialize.
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
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798402"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="1d0e8-103">Função de proxy de \_ inicialização IWICBitmapScaler \_</span><span class="sxs-lookup"><span data-stu-id="1d0e8-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="1d0e8-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1d0e8-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d0e8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="1d0e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d0e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0e8-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e8-108">Tipo: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="1d0e8-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="1d0e8-109">Ponteiro para este objeto [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="1d0e8-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="1d0e8-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e8-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="1d0e8-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="1d0e8-112">A origem do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d0e8-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="1d0e8-113">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e8-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1d0e8-114">Type: **UINT**</span></span>

<span data-ttu-id="1d0e8-115">A largura de destino.</span><span class="sxs-lookup"><span data-stu-id="1d0e8-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="1d0e8-116">*uiHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e8-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1d0e8-117">Type: **UINT**</span></span>

<span data-ttu-id="1d0e8-118">A altura de destino.</span><span class="sxs-lookup"><span data-stu-id="1d0e8-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="1d0e8-119">*modo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0e8-120">Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="1d0e8-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="1d0e8-121">O modo de interpolação a ser usado ao Dimensionar.</span><span class="sxs-lookup"><span data-stu-id="1d0e8-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0e8-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d0e8-122">Return value</span></span>

<span data-ttu-id="1d0e8-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1d0e8-123">Type: **HRESULT**</span></span>

<span data-ttu-id="1d0e8-124">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1d0e8-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d0e8-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d0e8-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0e8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d0e8-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0e8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0e8-127">Requirements</span></span>



| <span data-ttu-id="1d0e8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0e8-128">Requirement</span></span> | <span data-ttu-id="1d0e8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1d0e8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0e8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d0e8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0e8-131">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1d0e8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d0e8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0e8-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d0e8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1d0e8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1d0e8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d0e8-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d0e8-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




