---
description: Função de proxy para o método resolution.
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
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768300"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="af27f-103">\_Função de proxy resolution do IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="af27f-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="af27f-104">Função de proxy para o método [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="af27f-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="af27f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af27f-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="af27f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af27f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af27f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="af27f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af27f-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="af27f-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="af27f-109">Ponteiro para este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="af27f-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="af27f-110">*DpiX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af27f-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af27f-111">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="af27f-111">Type: **double**</span></span>

<span data-ttu-id="af27f-112">A resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="af27f-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="af27f-113">*DpiY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af27f-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af27f-114">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="af27f-114">Type: **double**</span></span>

<span data-ttu-id="af27f-115">A resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="af27f-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af27f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af27f-116">Return value</span></span>

<span data-ttu-id="af27f-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="af27f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="af27f-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af27f-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af27f-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af27f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af27f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="af27f-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="af27f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af27f-121">Requirements</span></span>



| <span data-ttu-id="af27f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="af27f-122">Requirement</span></span> | <span data-ttu-id="af27f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="af27f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af27f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af27f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af27f-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af27f-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="af27f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af27f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af27f-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af27f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="af27f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="af27f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af27f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af27f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




