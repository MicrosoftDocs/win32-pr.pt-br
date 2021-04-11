---
description: O método IsChildOf determina se uma solicitação é um filho de uma solicitação especificada (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Método IWbemCausalityAccess:: IsChildOf (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170607"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="433f1-103">Método IWbemCausalityAccess:: IsChildOf</span><span class="sxs-lookup"><span data-stu-id="433f1-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="433f1-104">O método **IsChildOf** determina se uma solicitação é um filho de uma solicitação especificada (PID).</span><span class="sxs-lookup"><span data-stu-id="433f1-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="433f1-105">Uma solicitação pai pode ter várias solicitações filho.</span><span class="sxs-lookup"><span data-stu-id="433f1-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="433f1-106">Cada solicitação é identificada por um GUID (identificador global exclusivo) e pode ter uma solicitação pai ou pode ser uma solicitação superior.</span><span class="sxs-lookup"><span data-stu-id="433f1-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="433f1-107">Um GUID é um número de bits de 128 exclusivo.</span><span class="sxs-lookup"><span data-stu-id="433f1-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="433f1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="433f1-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="433f1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="433f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="433f1-110">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="433f1-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="433f1-111">O valor de GUID que identifica exclusivamente uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="433f1-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="433f1-112">Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="433f1-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="433f1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="433f1-113">Return value</span></span>

<span data-ttu-id="433f1-114">Retornará com êxito se a solicitação especificada for um filho da solicitação que chama o método **IsChildOf** .</span><span class="sxs-lookup"><span data-stu-id="433f1-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="433f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="433f1-115">Requirements</span></span>



| <span data-ttu-id="433f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="433f1-116">Requirement</span></span> | <span data-ttu-id="433f1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="433f1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="433f1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="433f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="433f1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="433f1-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="433f1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="433f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="433f1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="433f1-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="433f1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="433f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="433f1-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="433f1-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="433f1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="433f1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="433f1-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="433f1-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433f1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="433f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433f1-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="433f1-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




