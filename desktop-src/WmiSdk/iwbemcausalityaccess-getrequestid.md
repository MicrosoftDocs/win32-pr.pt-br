---
description: O método getsolicitid retorna um valor de GUID (identificador global exclusivo) para uma solicitação. Um GUID é um número de bits de 128 exclusivo.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Método IWbemCausalityAccess:: getsolicitid (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767712"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="8c562-104">Método IWbemCausalityAccess:: getsolicitid</span><span class="sxs-lookup"><span data-stu-id="8c562-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="8c562-105">O método **Getsolicitid** retorna um valor de GUID (identificador global exclusivo) para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c562-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="8c562-106">Um GUID é um número de bits de 128 exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8c562-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c562-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c562-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="8c562-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c562-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c562-109">*pid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8c562-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c562-110">O valor de GUID que identifica exclusivamente uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8c562-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="8c562-111">Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="8c562-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c562-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c562-112">Return value</span></span>

<span data-ttu-id="8c562-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8c562-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c562-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c562-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c562-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c562-115">Requirements</span></span>



| <span data-ttu-id="8c562-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c562-116">Requirement</span></span> | <span data-ttu-id="8c562-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8c562-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c562-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c562-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8c562-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c562-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c562-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c562-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8c562-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c562-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c562-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c562-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c562-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c562-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="8c562-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8c562-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c562-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c562-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c562-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c562-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c562-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="8c562-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




