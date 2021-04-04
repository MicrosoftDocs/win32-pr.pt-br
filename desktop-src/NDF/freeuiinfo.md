---
title: Função FreeUiInfo (Ndattributils. h)
description: Desaloca a memória alocada internamente para uma estrutura UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- NDF da função FreeUiInfo
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085366"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="de124-104">Função FreeUiInfo</span><span class="sxs-lookup"><span data-stu-id="de124-104">FreeUiInfo function</span></span>

<span data-ttu-id="de124-105">A função **FreeUiInfo** Desaloca a memória alocada internamente para uma estrutura [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) .</span><span class="sxs-lookup"><span data-stu-id="de124-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="de124-106">Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.</span><span class="sxs-lookup"><span data-stu-id="de124-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="de124-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de124-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de124-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de124-109">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de124-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de124-110">Tipo: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="de124-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="de124-111">A estrutura.</span><span class="sxs-lookup"><span data-stu-id="de124-111">The structure.</span></span> <span data-ttu-id="de124-112">A memória alocada apontada por essa estrutura será liberada.</span><span class="sxs-lookup"><span data-stu-id="de124-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de124-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de124-113">Return value</span></span>

<span data-ttu-id="de124-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="de124-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="de124-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de124-115">Requirements</span></span>



| <span data-ttu-id="de124-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de124-116">Requirement</span></span> | <span data-ttu-id="de124-117">Valor</span><span class="sxs-lookup"><span data-stu-id="de124-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="de124-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de124-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de124-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="de124-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="de124-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de124-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de124-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="de124-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="de124-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de124-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de124-123"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="de124-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de124-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="de124-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de124-125">_ *UiInfo*\*</span><span class="sxs-lookup"><span data-stu-id="de124-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="de124-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="de124-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

