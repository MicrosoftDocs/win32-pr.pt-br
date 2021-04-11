---
description: Função de proxy para o método GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: Função IWICBitmapCodecInfo_GetFileExtensions_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296295"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="88e21-103">\_Função de \_ proxy IWICBitmapCodecInfo GetFileExtensions</span><span class="sxs-lookup"><span data-stu-id="88e21-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="88e21-104">Função de proxy para o método [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .</span><span class="sxs-lookup"><span data-stu-id="88e21-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e21-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88e21-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="88e21-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88e21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e21-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="88e21-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88e21-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="88e21-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="88e21-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="88e21-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="88e21-110">*cchFileExtensions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88e21-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88e21-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="88e21-111">Type: **UINT**</span></span>

<span data-ttu-id="88e21-112">O tamanho do buffer de extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="88e21-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="88e21-113">*wzFileExtensions* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="88e21-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="88e21-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="88e21-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="88e21-115">Um ponteiro que recebe as extensões de nome de arquivo associadas ao codec.</span><span class="sxs-lookup"><span data-stu-id="88e21-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="88e21-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="88e21-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="88e21-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="88e21-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="88e21-118">O tamanho real do buffer necessário para recuperar todas as extensões de nome de arquivo associadas ao codec.</span><span class="sxs-lookup"><span data-stu-id="88e21-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e21-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88e21-119">Return value</span></span>

<span data-ttu-id="88e21-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="88e21-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="88e21-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88e21-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88e21-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88e21-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88e21-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="88e21-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="88e21-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e21-124">Requirements</span></span>



| <span data-ttu-id="88e21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e21-125">Requirement</span></span> | <span data-ttu-id="88e21-126">Valor</span><span class="sxs-lookup"><span data-stu-id="88e21-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e21-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e21-127">Minimum supported client</span></span><br/> | <span data-ttu-id="88e21-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88e21-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="88e21-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e21-129">Minimum supported server</span></span><br/> | <span data-ttu-id="88e21-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88e21-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="88e21-131">DLL</span><span class="sxs-lookup"><span data-stu-id="88e21-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88e21-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88e21-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




