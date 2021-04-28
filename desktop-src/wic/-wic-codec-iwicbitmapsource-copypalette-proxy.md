---
description: Função de proxy de função IWICBitmapSource_CopyPalette_Proxy para o método CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Função IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ad9f5096aff7770a0b1624495c5c717440b6bd39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100494"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="c1762-103">\_Função de \_ proxy IWICBitmapSource CopyPalette</span><span class="sxs-lookup"><span data-stu-id="c1762-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="c1762-104">Função de proxy para o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="c1762-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1762-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1762-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c1762-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1762-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1762-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c1762-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1762-108">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="c1762-108">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="c1762-109">Ponteiro para este objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="c1762-109">Pointer to this [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1762-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1762-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1762-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="c1762-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="c1762-112">A paleta.</span><span class="sxs-lookup"><span data-stu-id="c1762-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1762-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c1762-113">Return value</span></span>

<span data-ttu-id="c1762-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1762-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c1762-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c1762-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1762-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1762-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1762-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1762-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c1762-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1762-118">Requirements</span></span>



| <span data-ttu-id="c1762-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1762-119">Requirement</span></span> | <span data-ttu-id="c1762-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c1762-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1762-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1762-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1762-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1762-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c1762-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1762-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1762-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1762-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c1762-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c1762-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1762-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1762-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




