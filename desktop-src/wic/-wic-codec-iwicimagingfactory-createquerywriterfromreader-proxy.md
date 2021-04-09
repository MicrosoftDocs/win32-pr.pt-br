---
description: Função de proxy para o método CreateQueryWriterFromReader.
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: Função IWICImagingFactory_CreateQueryWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922563"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="3244d-103">\_Função de \_ proxy IWICImagingFactory CreateQueryWriterFromReader</span><span class="sxs-lookup"><span data-stu-id="3244d-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="3244d-104">Função de proxy para o método [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="3244d-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3244d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3244d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="3244d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3244d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3244d-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3244d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3244d-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="3244d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="3244d-109">_pIQueryReader \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3244d-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3244d-110">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="3244d-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="3244d-111">O leitor de consulta de metadados do qual criar o gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="3244d-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="3244d-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3244d-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3244d-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="3244d-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="3244d-114">O GUID do fornecedor para o gravador de consulta de metadados.</span><span class="sxs-lookup"><span data-stu-id="3244d-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="3244d-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3244d-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3244d-116">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="3244d-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="3244d-117">Um ponteiro que recebe um ponteiro para um novo [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="3244d-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3244d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3244d-118">Return value</span></span>

<span data-ttu-id="3244d-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3244d-119">Type: **HRESULT**</span></span>

<span data-ttu-id="3244d-120">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3244d-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3244d-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3244d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3244d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3244d-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3244d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3244d-123">Requirements</span></span>



| <span data-ttu-id="3244d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3244d-124">Requirement</span></span> | <span data-ttu-id="3244d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3244d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3244d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3244d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3244d-127">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3244d-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3244d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3244d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3244d-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3244d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3244d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3244d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3244d-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3244d-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




