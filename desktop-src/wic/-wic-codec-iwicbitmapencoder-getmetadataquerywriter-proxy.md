---
description: Função de proxy para o método GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: Função IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810659"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="0c4d9-103">\_Função de \_ proxy IWICBitmapEncoder GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="0c4d9-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="0c4d9-104">Função de proxy para o método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="0c4d9-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4d9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c4d9-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="0c4d9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c4d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4d9-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="0c4d9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c4d9-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="0c4d9-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="0c4d9-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="0c4d9-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0c4d9-110">*ppIMetadataQueryWriter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0c4d9-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c4d9-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="0c4d9-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="0c4d9-112">Um ponteiro que recebe um ponteiro para um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="0c4d9-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4d9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c4d9-113">Return value</span></span>

<span data-ttu-id="0c4d9-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c4d9-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0c4d9-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c4d9-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c4d9-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c4d9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4d9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c4d9-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4d9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c4d9-118">Requirements</span></span>



| <span data-ttu-id="0c4d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c4d9-119">Requirement</span></span> | <span data-ttu-id="0c4d9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0c4d9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4d9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c4d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4d9-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c4d9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0c4d9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c4d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4d9-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c4d9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0c4d9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c4d9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c4d9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c4d9-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




