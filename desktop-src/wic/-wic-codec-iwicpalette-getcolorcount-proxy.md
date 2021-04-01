---
description: Função de proxy para o método GetColorCount.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: Função IWICPalette_GetColorCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829213"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="2306f-103">\_Função de \_ proxy IWICPalette GetColorCount</span><span class="sxs-lookup"><span data-stu-id="2306f-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="2306f-104">Função de proxy para o método [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .</span><span class="sxs-lookup"><span data-stu-id="2306f-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2306f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2306f-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="2306f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2306f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2306f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="2306f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2306f-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="2306f-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="2306f-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="2306f-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="2306f-110">*pcCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2306f-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2306f-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="2306f-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="2306f-112">Ponteiro que recebe o número de cores na tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="2306f-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2306f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2306f-113">Return value</span></span>

<span data-ttu-id="2306f-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2306f-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2306f-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2306f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2306f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2306f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2306f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2306f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2306f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2306f-118">Requirements</span></span>



| <span data-ttu-id="2306f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2306f-119">Requirement</span></span> | <span data-ttu-id="2306f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2306f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2306f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2306f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2306f-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2306f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2306f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2306f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2306f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2306f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2306f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2306f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2306f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2306f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




