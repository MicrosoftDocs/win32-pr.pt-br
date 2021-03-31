---
description: Função de proxy para o método InitializePredefined.
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: Função IWICPalette_InitializePredefined_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662938"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="6df36-103">\_Função de \_ proxy IWICPalette InitializePredefined</span><span class="sxs-lookup"><span data-stu-id="6df36-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="6df36-104">Função de proxy para o método [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) .</span><span class="sxs-lookup"><span data-stu-id="6df36-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df36-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="6df36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df36-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6df36-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df36-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="6df36-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="6df36-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="6df36-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="6df36-110">*ePaletteType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6df36-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df36-111">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="6df36-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="6df36-112">O tipo de paleta predefinido desejado.</span><span class="sxs-lookup"><span data-stu-id="6df36-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="6df36-113">*fAddTransparentColor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6df36-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df36-114">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="6df36-114">Type: **BOOL**</span></span>

<span data-ttu-id="6df36-115">A cor de transparente opcional a ser adicionada à paleta.</span><span class="sxs-lookup"><span data-stu-id="6df36-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="6df36-116">Se nenhuma cor transparente for necessária, use 0.</span><span class="sxs-lookup"><span data-stu-id="6df36-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df36-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6df36-117">Return value</span></span>

<span data-ttu-id="6df36-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6df36-118">Type: **HRESULT**</span></span>

<span data-ttu-id="6df36-119">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6df36-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6df36-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6df36-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df36-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6df36-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6df36-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df36-122">Requirements</span></span>



| <span data-ttu-id="6df36-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df36-123">Requirement</span></span> | <span data-ttu-id="6df36-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6df36-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df36-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6df36-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6df36-126">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6df36-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6df36-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6df36-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6df36-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6df36-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6df36-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6df36-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6df36-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df36-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




