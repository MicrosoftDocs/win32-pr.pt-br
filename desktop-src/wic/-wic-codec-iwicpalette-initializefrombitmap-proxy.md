---
description: Função de proxy para o método InitializeFromBitmap.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: Função IWICPalette_InitializeFromBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765762"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="b9418-103">\_Função de \_ proxy IWICPalette InitializeFromBitmap</span><span class="sxs-lookup"><span data-stu-id="b9418-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="b9418-104">Função de proxy para o método [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) .</span><span class="sxs-lookup"><span data-stu-id="b9418-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9418-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9418-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="b9418-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9418-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="b9418-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9418-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b9418-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b9418-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="b9418-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="b9418-110">*pISurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9418-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9418-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b9418-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b9418-112">Ponteiro para o bitmap de origem.</span><span class="sxs-lookup"><span data-stu-id="b9418-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b9418-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9418-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9418-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b9418-114">Type: **UINT**</span></span>

<span data-ttu-id="b9418-115">O número de cores com as quais inicializar a paleta.</span><span class="sxs-lookup"><span data-stu-id="b9418-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="b9418-116">*fAddTransparentColor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9418-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9418-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="b9418-117">Type: **BOOL**</span></span>

<span data-ttu-id="b9418-118">Um valor para indicar se uma cor transparente deve ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="b9418-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9418-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9418-119">Return value</span></span>

<span data-ttu-id="b9418-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9418-120">Type: **HRESULT**</span></span>

<span data-ttu-id="b9418-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9418-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9418-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9418-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9418-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9418-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b9418-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9418-124">Requirements</span></span>



| <span data-ttu-id="b9418-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9418-125">Requirement</span></span> | <span data-ttu-id="b9418-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b9418-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9418-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9418-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9418-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9418-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b9418-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9418-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9418-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9418-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b9418-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b9418-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9418-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9418-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




