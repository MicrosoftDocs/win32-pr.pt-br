---
description: Função de proxy para o método getLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: Função IWICMetadataQueryReader_GetLocation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758558"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="0c9aa-103">\_Função de proxy getLocation do IWICMetadataQueryReader \_</span><span class="sxs-lookup"><span data-stu-id="0c9aa-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="0c9aa-104">Função de proxy para o método [**getLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .</span><span class="sxs-lookup"><span data-stu-id="0c9aa-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c9aa-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="0c9aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c9aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c9aa-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c9aa-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="0c9aa-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="0c9aa-109">Ponteiro para este objeto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="0c9aa-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="0c9aa-110">*cchMaxLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c9aa-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0c9aa-111">Type: **UINT**</span></span>

<span data-ttu-id="0c9aa-112">O comprimento do buffer *wzNamespace* .</span><span class="sxs-lookup"><span data-stu-id="0c9aa-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0c9aa-113">*wzNamespace* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c9aa-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0c9aa-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="0c9aa-115">Ponteiro que recebe o local do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="0c9aa-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="0c9aa-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c9aa-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="0c9aa-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="0c9aa-118">O tamanho real do buffer necessário para recuperar o local do namespace atual.</span><span class="sxs-lookup"><span data-stu-id="0c9aa-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c9aa-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c9aa-119">Return value</span></span>

<span data-ttu-id="0c9aa-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0c9aa-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0c9aa-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c9aa-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c9aa-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c9aa-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c9aa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c9aa-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0c9aa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c9aa-124">Requirements</span></span>



| <span data-ttu-id="0c9aa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c9aa-125">Requirement</span></span> | <span data-ttu-id="0c9aa-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0c9aa-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9aa-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c9aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0c9aa-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0c9aa-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c9aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0c9aa-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c9aa-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0c9aa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0c9aa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c9aa-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c9aa-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




