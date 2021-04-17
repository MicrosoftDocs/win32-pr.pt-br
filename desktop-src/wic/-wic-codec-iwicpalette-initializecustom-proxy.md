---
description: Função de proxy para o método InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: Função IWICPalette_InitializeCustom_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811729"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="14708-103">\_Função de \_ proxy IWICPalette InitializeCustom</span><span class="sxs-lookup"><span data-stu-id="14708-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="14708-104">Função de proxy para o método [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .</span><span class="sxs-lookup"><span data-stu-id="14708-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14708-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14708-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="14708-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14708-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="14708-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14708-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="14708-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="14708-109">Ponteiro para este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="14708-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="14708-110">*pColors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14708-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14708-111">Tipo: \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="14708-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="14708-112">Ponteiro para a matriz de cores.</span><span class="sxs-lookup"><span data-stu-id="14708-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="14708-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14708-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14708-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="14708-114">Type: **UINT**</span></span>

<span data-ttu-id="14708-115">O número de cores em *pColors*.</span><span class="sxs-lookup"><span data-stu-id="14708-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14708-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14708-116">Return value</span></span>

<span data-ttu-id="14708-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14708-117">Type: **HRESULT**</span></span>

<span data-ttu-id="14708-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="14708-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14708-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14708-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14708-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="14708-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14708-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14708-121">Requirements</span></span>



| <span data-ttu-id="14708-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14708-122">Requirement</span></span> | <span data-ttu-id="14708-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14708-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14708-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14708-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14708-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14708-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14708-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14708-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14708-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14708-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14708-128">DLL</span><span class="sxs-lookup"><span data-stu-id="14708-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14708-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14708-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




