---
description: Função de proxy para o método HasAlpha.
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: Função IWICPalette_HasAlpha_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922154"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="7ceea-103">\_Função de \_ proxy IWICPalette HasAlpha</span><span class="sxs-lookup"><span data-stu-id="7ceea-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="7ceea-104">Função de proxy para o método [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) .</span><span class="sxs-lookup"><span data-stu-id="7ceea-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ceea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ceea-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="7ceea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ceea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ceea-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="7ceea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ceea-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="7ceea-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="7ceea-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="7ceea-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ceea-110">*pfHasAlpha* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7ceea-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ceea-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="7ceea-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="7ceea-112">Ponteiro que recebe `TRUE` se a paleta contém uma cor transparente; caso contrário, `FALSE` .</span><span class="sxs-lookup"><span data-stu-id="7ceea-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ceea-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ceea-113">Return value</span></span>

<span data-ttu-id="7ceea-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7ceea-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7ceea-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ceea-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ceea-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ceea-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ceea-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ceea-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7ceea-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ceea-118">Requirements</span></span>



| <span data-ttu-id="7ceea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ceea-119">Requirement</span></span> | <span data-ttu-id="7ceea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7ceea-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceea-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ceea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ceea-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ceea-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7ceea-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ceea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ceea-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ceea-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7ceea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ceea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ceea-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ceea-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




