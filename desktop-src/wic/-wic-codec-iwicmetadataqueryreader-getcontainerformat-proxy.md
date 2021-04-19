---
description: Função de proxy para o método GetContainerFormat.
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
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764397"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="c0e98-103">\_Função de \_ proxy IWICMetadataQueryReader GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="c0e98-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="c0e98-104">Função de proxy para o método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="c0e98-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e98-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0e98-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c0e98-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0e98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e98-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="c0e98-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0e98-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="c0e98-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="c0e98-109">Ponteiro para este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="c0e98-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="c0e98-110">*pguidContainerFormat* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0e98-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0e98-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="c0e98-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="c0e98-112">Ponteiro que recebe o GUID de formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="c0e98-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e98-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0e98-113">Return value</span></span>

<span data-ttu-id="c0e98-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c0e98-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c0e98-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c0e98-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0e98-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0e98-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e98-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0e98-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e98-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0e98-118">Requirements</span></span>



| <span data-ttu-id="c0e98-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0e98-119">Requirement</span></span> | <span data-ttu-id="c0e98-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c0e98-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e98-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0e98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0e98-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0e98-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c0e98-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0e98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0e98-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0e98-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c0e98-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e98-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0e98-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0e98-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




