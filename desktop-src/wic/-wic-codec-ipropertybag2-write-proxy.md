---
description: 'Função de proxy do Windows Imaging Component (WIC) para IPropertyBag2:: Write.'
ms.assetid: b97caba6-298a-4b36-9f39-9b5440b866c3
title: Função IPropertyBag2_Write_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertyBag2_Write_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c868ee748c3c2894daa63850284ae121f85975fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296299"
---
# <a name="ipropertybag2_write_proxy-function"></a><span data-ttu-id="60ab0-103">Função de proxy de \_ gravação IPropertyBag2 \_</span><span class="sxs-lookup"><span data-stu-id="60ab0-103">IPropertyBag2\_Write\_Proxy function</span></span>

<span data-ttu-id="60ab0-104">Função de proxy do Windows Imaging Component (WIC) para IPropertyBag2:: Write.</span><span class="sxs-lookup"><span data-stu-id="60ab0-104">Windows Imaging Component (WIC) proxy function for IPropertyBag2::Write.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ab0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60ab0-105">Syntax</span></span>


```C++
HRESULT IPropertyBag2_Write_Proxy(
  _In_ IPropertyBag2 *THIS_PTR,
  _In_ ULONG         cProperties,
  _In_ PROPBAG2      *ppropBag,
  _In_ VARIANT       *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="60ab0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60ab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ab0-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ab0-108">Tipo: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="60ab0-108">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="60ab0-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="60ab0-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="60ab0-110">_cProperties \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-110">_cProperties\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ab0-111">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="60ab0-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="60ab0-112">*ppropBag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-112">*ppropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ab0-113">Tipo: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="60ab0-113">Type: \**[PROPBAG2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85))\** _</span></span>

</dd> <dt>

<span data-ttu-id="60ab0-114">_pvarValue \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-114">_pvarValue\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ab0-115">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="60ab0-115">Type: \**VARIANT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ab0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60ab0-116">Return value</span></span>

<span data-ttu-id="60ab0-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="60ab0-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="60ab0-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60ab0-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60ab0-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60ab0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ab0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="60ab0-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="60ab0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60ab0-121">Requirements</span></span>



| <span data-ttu-id="60ab0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ab0-122">Requirement</span></span> | <span data-ttu-id="60ab0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="60ab0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ab0-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ab0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="60ab0-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="60ab0-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60ab0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="60ab0-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60ab0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="60ab0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="60ab0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60ab0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60ab0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

