---
description: IWICBitmap_SetResolution_Proxy função de proxy de função para o método resolution.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: Função IWICBitmap_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086374"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="bc231-103">\_Função de proxy resolution do IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="bc231-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="bc231-104">Função de proxy para o método [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="bc231-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc231-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc231-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="bc231-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc231-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc231-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="bc231-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc231-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="bc231-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="bc231-109">Ponteiro para este objeto [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="bc231-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="bc231-110">*DpiX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc231-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc231-111">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="bc231-111">Type: **double**</span></span>

<span data-ttu-id="bc231-112">A resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="bc231-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="bc231-113">*DpiY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc231-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc231-114">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="bc231-114">Type: **double**</span></span>

<span data-ttu-id="bc231-115">A resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="bc231-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc231-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bc231-116">Return value</span></span>

<span data-ttu-id="bc231-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc231-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bc231-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc231-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc231-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc231-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc231-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc231-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bc231-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc231-121">Requirements</span></span>



| <span data-ttu-id="bc231-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc231-122">Requirement</span></span> | <span data-ttu-id="bc231-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bc231-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc231-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc231-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc231-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc231-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bc231-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc231-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc231-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc231-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bc231-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bc231-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc231-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc231-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




