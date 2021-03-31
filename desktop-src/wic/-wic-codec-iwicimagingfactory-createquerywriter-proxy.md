---
description: Função de proxy para o método CreateQueryWriter.
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: Função IWICImagingFactory_CreateQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663009"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="d961e-103">\_Função de \_ proxy IWICImagingFactory CreateQueryWriter</span><span class="sxs-lookup"><span data-stu-id="d961e-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="d961e-104">Função de proxy para o método [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="d961e-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d961e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d961e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="d961e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d961e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d961e-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d961e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d961e-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d961e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d961e-109">_guidMetadataFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d961e-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d961e-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="d961e-110">Type: **REFGUID**</span></span>

<span data-ttu-id="d961e-111">O GUID para o formato de metadados desejado.</span><span class="sxs-lookup"><span data-stu-id="d961e-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="d961e-112">*pguidVendor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d961e-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d961e-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="d961e-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="d961e-114">O GUID do fornecedor do gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="d961e-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="d961e-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d961e-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d961e-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="d961e-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="d961e-117">Um ponteiro que recebe um ponteiro para um novo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="d961e-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d961e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d961e-118">Return value</span></span>

<span data-ttu-id="d961e-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d961e-119">Type: **HRESULT**</span></span>

<span data-ttu-id="d961e-120">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d961e-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d961e-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d961e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d961e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d961e-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d961e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d961e-123">Requirements</span></span>



| <span data-ttu-id="d961e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d961e-124">Requirement</span></span> | <span data-ttu-id="d961e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d961e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d961e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d961e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d961e-127">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d961e-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d961e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d961e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d961e-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d961e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d961e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d961e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d961e-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d961e-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




