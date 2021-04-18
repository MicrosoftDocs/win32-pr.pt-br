---
description: 'Função de proxy do Windows Imaging Component (WIC) para IEnumString:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: Função IEnumString_Reset_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788660"
---
# <a name="ienumstring_reset_wic_proxy-function"></a><span data-ttu-id="10016-103">\_Função de \_ proxy WIC de redefinição de IEnumString \_</span><span class="sxs-lookup"><span data-stu-id="10016-103">IEnumString\_Reset\_WIC\_Proxy function</span></span>

<span data-ttu-id="10016-104">Função de proxy do Windows Imaging Component (WIC) para IEnumString:: Reset.</span><span class="sxs-lookup"><span data-stu-id="10016-104">Windows Imaging Component (WIC) proxy function for IEnumString::Reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="10016-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10016-105">Syntax</span></span>


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="10016-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10016-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="10016-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10016-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="10016-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="10016-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="10016-109">PARAMDESC</span></span>

</dd> <dt>

<span data-ttu-id="10016-110">_celt \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10016-110">_celt\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10016-111">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="10016-111">Type: **ULONG**</span></span>

</dd> <dt>

<span data-ttu-id="10016-112">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10016-112">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10016-113">Tipo: \**LPOLESTR \** _</span><span class="sxs-lookup"><span data-stu-id="10016-113">Type: \**LPOLESTR\** _</span></span>

</dd> <dt>

<span data-ttu-id="10016-114">_pceltFetched \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="10016-114">_pceltFetched\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10016-115">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="10016-115">Type: \**ULONG\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10016-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10016-116">Return value</span></span>

<span data-ttu-id="10016-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="10016-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="10016-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="10016-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10016-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10016-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="10016-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="10016-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="10016-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10016-121">Requirements</span></span>



| <span data-ttu-id="10016-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="10016-122">Requirement</span></span> | <span data-ttu-id="10016-123">Valor</span><span class="sxs-lookup"><span data-stu-id="10016-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10016-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10016-124">Minimum supported client</span></span><br/> | <span data-ttu-id="10016-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10016-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="10016-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10016-126">Minimum supported server</span></span><br/> | <span data-ttu-id="10016-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="10016-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="10016-128">DLL</span><span class="sxs-lookup"><span data-stu-id="10016-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10016-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10016-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




