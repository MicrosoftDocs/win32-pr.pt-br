---
description: Recupera o tipo de relação que esse IContextLink representa.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Método IContextLink:: GetContextLinkDirection (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164550"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="9cdf6-103">Método IContextLink:: GetContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="9cdf6-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="9cdf6-104">Recupera o tipo de relação que esse [**IContextLink**](icontextlink.md) representa.</span><span class="sxs-lookup"><span data-stu-id="9cdf6-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cdf6-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="9cdf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cdf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cdf6-107">*pContextLinkDirection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cdf6-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cdf6-108">A direção que esse [**IContextLink**](icontextlink.md) representa.</span><span class="sxs-lookup"><span data-stu-id="9cdf6-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cdf6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cdf6-109">Return value</span></span>

<span data-ttu-id="9cdf6-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9cdf6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdf6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cdf6-111">Requirements</span></span>



| <span data-ttu-id="9cdf6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cdf6-112">Requirement</span></span> | <span data-ttu-id="9cdf6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9cdf6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdf6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cdf6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdf6-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9cdf6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9cdf6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cdf6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdf6-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9cdf6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9cdf6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cdf6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cdf6-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdf6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9cdf6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9cdf6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cdf6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cdf6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9cdf6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cdf6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cdf6-123">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="9cdf6-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="9cdf6-124">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="9cdf6-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="9cdf6-125">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="9cdf6-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




