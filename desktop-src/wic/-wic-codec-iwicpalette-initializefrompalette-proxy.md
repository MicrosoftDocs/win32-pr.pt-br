---
description: Função de proxy para o método InitializeFromPalette.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: Função IWICPalette_InitializeFromPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836884"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="d735d-103">\_Função de \_ proxy IWICPalette InitializeFromPalette</span><span class="sxs-lookup"><span data-stu-id="d735d-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="d735d-104">Função de proxy para o método [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .</span><span class="sxs-lookup"><span data-stu-id="d735d-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d735d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d735d-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="d735d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d735d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d735d-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="d735d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d735d-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="d735d-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="d735d-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="d735d-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="d735d-110">*pIMILPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d735d-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d735d-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="d735d-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="d735d-112">Ponteiro para a paleta de origem.</span><span class="sxs-lookup"><span data-stu-id="d735d-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d735d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d735d-113">Return value</span></span>

<span data-ttu-id="d735d-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d735d-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d735d-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d735d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d735d-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d735d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d735d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d735d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d735d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d735d-118">Requirements</span></span>



| <span data-ttu-id="d735d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d735d-119">Requirement</span></span> | <span data-ttu-id="d735d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d735d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d735d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d735d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d735d-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d735d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d735d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d735d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d735d-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d735d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d735d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d735d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d735d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d735d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




