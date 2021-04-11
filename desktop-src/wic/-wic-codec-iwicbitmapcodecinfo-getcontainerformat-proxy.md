---
description: Função de proxy para o método GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: Função IWICBitmapCodecInfo_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164425"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="63483-103">\_Função de \_ proxy IWICBitmapCodecInfo GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="63483-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="63483-104">Função de proxy para o método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="63483-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63483-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63483-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="63483-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63483-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="63483-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63483-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="63483-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="63483-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="63483-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="63483-110">*pguidContainerFormat* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="63483-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63483-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="63483-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="63483-112">Um ponteiro que recebe o GUID do contêiner.</span><span class="sxs-lookup"><span data-stu-id="63483-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63483-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63483-113">Return value</span></span>

<span data-ttu-id="63483-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="63483-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="63483-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="63483-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63483-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63483-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63483-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="63483-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="63483-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63483-118">Requirements</span></span>



| <span data-ttu-id="63483-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63483-119">Requirement</span></span> | <span data-ttu-id="63483-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63483-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63483-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63483-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63483-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63483-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="63483-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63483-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63483-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63483-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="63483-125">DLL</span><span class="sxs-lookup"><span data-stu-id="63483-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63483-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63483-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




