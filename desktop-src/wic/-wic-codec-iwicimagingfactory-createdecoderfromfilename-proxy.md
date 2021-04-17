---
description: Função de proxy para o método CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: Função IWICImagingFactory_CreateDecoderFromFilename_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763225"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="a8d3f-103">\_Função de \_ proxy IWICImagingFactory CreateDecoderFromFilename</span><span class="sxs-lookup"><span data-stu-id="a8d3f-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="a8d3f-104">Função de proxy para o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="a8d3f-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8d3f-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="a8d3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8d3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d3f-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-108">Tipo: \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="a8d3f-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-109">_wzFilename \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-110">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="a8d3f-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um objeto a ser criado ou aberto.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-112">*pguidVendor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="a8d3f-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="a8d3f-114">O GUID do fornecedor para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-115">_dwDesiredAccess \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-116">Type: **DWORD**</span></span>

<span data-ttu-id="a8d3f-117">O acesso ao objeto, que pode ser lido, gravado ou ambos.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="a8d3f-118">Para obter mais informações, consulte [segurança de arquivos e \[ arquivos \] de direitos de acesso](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-119">*metadataoptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-120">Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="a8d3f-121">O [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) a ser usado ao criar o decodificador.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-122">*ppIDecoder* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d3f-123">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="a8d3f-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="a8d3f-124">Um ponteiro que recebe um ponteiro para o novo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d3f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8d3f-125">Return value</span></span>

<span data-ttu-id="a8d3f-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="a8d3f-127">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a8d3f-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8d3f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d3f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8d3f-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d3f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d3f-130">Requirements</span></span>



| <span data-ttu-id="a8d3f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d3f-131">Requirement</span></span> | <span data-ttu-id="a8d3f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d3f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d3f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d3f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d3f-134">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a8d3f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d3f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d3f-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8d3f-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a8d3f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d3f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d3f-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8d3f-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

