---
description: Função de proxy de função IWICBitmapDecoder_CopyPalette_Proxy para o método CopyPalette.
ms.assetid: 2775b389-d6e9-479c-93ea-147e4501551d
title: Função IWICBitmapDecoder_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56dbc523fe29ef9cc958b6ffbd80509284b78b88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086354"
---
# <a name="iwicbitmapdecoder_copypalette_proxy-function"></a><span data-ttu-id="0a641-103">\_Função de \_ proxy IWICBitmapDecoder CopyPalette</span><span class="sxs-lookup"><span data-stu-id="0a641-103">IWICBitmapDecoder\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="0a641-104">Função de proxy para o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="0a641-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a641-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a641-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_CopyPalette_Proxy(
  _In_ IWICBitmapDecoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="0a641-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a641-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a641-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="0a641-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a641-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="0a641-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="0a641-109">Ponteiro para este objeto [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="0a641-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0a641-110">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a641-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a641-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="0a641-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="0a641-112">A paleta de imagens a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="0a641-112">The image palette to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a641-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0a641-113">Return value</span></span>

<span data-ttu-id="0a641-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0a641-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0a641-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a641-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a641-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a641-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a641-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a641-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0a641-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a641-118">Requirements</span></span>



| <span data-ttu-id="0a641-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a641-119">Requirement</span></span> | <span data-ttu-id="0a641-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0a641-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a641-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a641-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a641-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a641-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0a641-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a641-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a641-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a641-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0a641-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a641-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a641-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a641-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




