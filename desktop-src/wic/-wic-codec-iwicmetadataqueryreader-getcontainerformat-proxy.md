---
description: Função de proxy de função IWICMetadataQueryReader_GetContainerFormat_Proxy para o método GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: Função IWICMetadataQueryReader_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097134"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="a5d8f-103">\_Função de \_ proxy IWICMetadataQueryReader GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="a5d8f-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="a5d8f-104">Função de proxy para o método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5d8f-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a5d8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5d8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d8f-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5d8f-108">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="a5d8f-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="a5d8f-109">Ponteiro para este objeto [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-110">*pguidContainerFormat* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5d8f-111">Tipo: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="a5d8f-111">Type: **GUID\***</span></span>

<span data-ttu-id="a5d8f-112">Ponteiro que recebe o GUID de formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d8f-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a5d8f-113">Return value</span></span>

<span data-ttu-id="a5d8f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a5d8f-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5d8f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d8f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5d8f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d8f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d8f-118">Requirements</span></span>



| <span data-ttu-id="a5d8f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d8f-119">Requirement</span></span> | <span data-ttu-id="a5d8f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a5d8f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d8f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5d8f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d8f-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a5d8f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5d8f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d8f-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a5d8f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d8f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d8f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




