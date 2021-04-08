---
description: Função de proxy para o método CreateMetadataWriterFromReader.
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: Função IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828731"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="09996-103">\_Função de \_ proxy IWICComponentFactory CreateMetadataWriterFromReader</span><span class="sxs-lookup"><span data-stu-id="09996-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="09996-104">Função de proxy para o método [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) .</span><span class="sxs-lookup"><span data-stu-id="09996-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09996-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09996-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="09996-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09996-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09996-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="09996-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09996-108">Tipo: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="09996-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="09996-109">Ponteiro para este objeto [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="09996-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="09996-110">*pIReader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09996-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09996-111">Tipo: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="09996-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="09996-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09996-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09996-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="09996-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="09996-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09996-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09996-115">Tipo: **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="09996-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09996-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09996-116">Return value</span></span>

<span data-ttu-id="09996-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09996-117">Type: **HRESULT**</span></span>

<span data-ttu-id="09996-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09996-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09996-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09996-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09996-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="09996-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="09996-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09996-121">Requirements</span></span>



| <span data-ttu-id="09996-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="09996-122">Requirement</span></span> | <span data-ttu-id="09996-123">Valor</span><span class="sxs-lookup"><span data-stu-id="09996-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09996-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09996-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09996-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09996-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="09996-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09996-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09996-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09996-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="09996-128">DLL</span><span class="sxs-lookup"><span data-stu-id="09996-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09996-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09996-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




