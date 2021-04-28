---
description: Função IWICBitmap_SetPalette_Proxy function-proxy para o método SetPalette.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Função IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086404"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="360fd-103">\_Função de proxy SetPalette IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="360fd-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="360fd-104">Função de proxy para o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="360fd-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="360fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="360fd-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="360fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="360fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360fd-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="360fd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="360fd-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="360fd-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="360fd-109">Ponteiro para este objeto [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="360fd-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="360fd-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="360fd-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="360fd-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="360fd-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="360fd-112">A paleta a ser usada para conversão.</span><span class="sxs-lookup"><span data-stu-id="360fd-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360fd-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="360fd-113">Return value</span></span>

<span data-ttu-id="360fd-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="360fd-114">Type: **HRESULT**</span></span>

<span data-ttu-id="360fd-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="360fd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="360fd-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="360fd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="360fd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="360fd-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="360fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="360fd-118">Requirements</span></span>



| <span data-ttu-id="360fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="360fd-119">Requirement</span></span> | <span data-ttu-id="360fd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="360fd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360fd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="360fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="360fd-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="360fd-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="360fd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="360fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="360fd-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="360fd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="360fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="360fd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="360fd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="360fd-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




