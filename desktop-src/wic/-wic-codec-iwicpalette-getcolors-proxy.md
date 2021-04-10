---
description: Função de proxy para o método getcolors.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: Função IWICPalette_GetColors_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170459"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="7ef5d-103">\_Função de proxy IWICPalette Getcolors \_</span><span class="sxs-lookup"><span data-stu-id="7ef5d-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="7ef5d-104">Função de proxy para o método [**Getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) .</span><span class="sxs-lookup"><span data-stu-id="7ef5d-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ef5d-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="7ef5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ef5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef5d-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef5d-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="7ef5d-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="7ef5d-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="7ef5d-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5d-110">*colorCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef5d-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7ef5d-111">Type: **UINT**</span></span>

<span data-ttu-id="7ef5d-112">O tamanho da matriz *pColors* .</span><span class="sxs-lookup"><span data-stu-id="7ef5d-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5d-113">*pColors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef5d-114">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="7ef5d-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="7ef5d-115">Ponteiro que recebe as cores da paleta.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5d-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef5d-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="7ef5d-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="7ef5d-118">O tamanho real necessário para obter as cores da paleta.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef5d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ef5d-119">Return value</span></span>

<span data-ttu-id="7ef5d-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7ef5d-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7ef5d-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ef5d-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ef5d-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ef5d-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef5d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef5d-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef5d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef5d-124">Requirements</span></span>



| <span data-ttu-id="7ef5d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef5d-125">Requirement</span></span> | <span data-ttu-id="7ef5d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7ef5d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef5d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef5d-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7ef5d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef5d-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ef5d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7ef5d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7ef5d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ef5d-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ef5d-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




