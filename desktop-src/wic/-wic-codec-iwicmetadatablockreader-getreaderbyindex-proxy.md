---
description: Função de proxy para o método GetReaderByIndex.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: Função IWICMetadataBlockReader_GetReaderByIndex_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748679"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="e8aba-103">\_Função de proxy GetReaderByIndex de IWICMetadataBlockReader \_</span><span class="sxs-lookup"><span data-stu-id="e8aba-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="e8aba-104">Função de proxy para o método [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) .</span><span class="sxs-lookup"><span data-stu-id="e8aba-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8aba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8aba-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="e8aba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8aba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8aba-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8aba-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="e8aba-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="e8aba-109">Ponteiro para este objeto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="e8aba-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="e8aba-110">*nIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8aba-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="e8aba-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="e8aba-112">*ppIMetadataReader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8aba-113">Tipo: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="e8aba-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8aba-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8aba-114">Return value</span></span>

<span data-ttu-id="e8aba-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e8aba-115">Type: **HRESULT**</span></span>

<span data-ttu-id="e8aba-116">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e8aba-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8aba-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e8aba-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8aba-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8aba-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e8aba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8aba-119">Requirements</span></span>



| <span data-ttu-id="e8aba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8aba-120">Requirement</span></span> | <span data-ttu-id="e8aba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8aba-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8aba-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8aba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8aba-123">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e8aba-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8aba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8aba-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8aba-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e8aba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e8aba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8aba-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8aba-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




